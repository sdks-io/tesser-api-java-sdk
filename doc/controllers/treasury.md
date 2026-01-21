# Treasury

```java
TreasuryController treasuryController = client.getTreasuryController();
```

## Class Name

`TreasuryController`

## Methods

* [Create Deposit](../../doc/controllers/treasury.md#create-deposit)
* [Create Withdrawal](../../doc/controllers/treasury.md#create-withdrawal)


# Create Deposit

Create a deposit payment.

```java
CompletableFuture<PaymentResponse> createDepositAsync(
    final String authorization,
    final CreateDepositRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`CreateDepositRequest`](../../doc/models/create-deposit-request.md) | Body, Required | - |

## Response Type

[`PaymentResponse`](../../doc/models/payment-response.md)

## Example Usage

```java
String authorization = "Bearer <token>";
CreateDepositRequest body = new CreateDepositRequest.Builder(
    "USD",
    "USDC",
    "44031e7e-d416-45f0-a46b-ded12b9751ca",
    "ETHEREUM"
)
.fromAmount("1000")
.build();

treasuryController.createDepositAsync(authorization, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Details coming soon | `ApiException` |


# Create Withdrawal

Create a withdrawal payment.

```java
CompletableFuture<PaymentResponse> createWithdrawalAsync(
    final String authorization,
    final CreateWithdrawalRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`CreateWithdrawalRequest`](../../doc/models/create-withdrawal-request.md) | Body, Required | - |

## Response Type

[`PaymentResponse`](../../doc/models/payment-response.md)

## Example Usage

```java
String authorization = "Bearer <token>";
CreateWithdrawalRequest body = new CreateWithdrawalRequest.Builder(
    "44031e7e-d416-45f0-a46b-ded12b9751ca",
    "USDC",
    "USD",
    "55042f8f-e527-56f1-b57c-eef23ca862db",
    "ETHEREUM"
)
.fromAmount("1000")
.build();

treasuryController.createWithdrawalAsync(authorization, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Details coming soon | `ApiException` |

