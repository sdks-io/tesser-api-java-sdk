# Experimental

```java
ExperimentalController experimentalController = client.getExperimentalController();
```

## Class Name

`ExperimentalController`


# Execute Payment

Accepts a signature for a payment step. Currently echoes the request, structured for future execution logic.

```java
CompletableFuture<PaymentResponse> executePaymentAsync(
    final String paymentId,
    final String stepId,
    final String authorization,
    final ExecutePaymentRequestDto body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paymentId` | `String` | Template, Required | Payment ID to execute. |
| `stepId` | `String` | Template, Required | Transfer step ID to execute. |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`ExecutePaymentRequestDto`](../../doc/models/execute-payment-request-dto.md) | Body, Required | - |

## Response Type

[`PaymentResponse`](../../doc/models/payment-response.md)

## Example Usage

```java
String paymentId = "payment_id0";
String stepId = "step_id4";
String authorization = "Bearer <token>";
ExecutePaymentRequestDto body = new ExecutePaymentRequestDto.Builder(
    "0xabcdef1234567890abcdef1234567890abcdef1234567890abcdef1234567890"
)
.turnkeyStamp(new TurnkeyStamp.Builder(
        "X-Stamp",
        "...",
        "..."
    )
    .build())
.build();

experimentalController.executePaymentAsync(paymentId, stepId, authorization, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

