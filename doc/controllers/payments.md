# Payments

```java
PaymentsController paymentsController = client.getPaymentsController();
```

## Class Name

`PaymentsController`

## Methods

* [Get Payments](../../doc/controllers/payments.md#get-payments)
* [Create Payment](../../doc/controllers/payments.md#create-payment)
* [Get Payment by Id](../../doc/controllers/payments.md#get-payment-by-id)
* [Update Payment](../../doc/controllers/payments.md#update-payment)
* [Review Payment](../../doc/controllers/payments.md#review-payment)


# Get Payments

Retrieve all payments for the authenticated user's organization.

```java
CompletableFuture<PaymentListResponse> getPaymentsAsync(
    final String authorization,
    final String startDate,
    final String endDate,
    final PaymentType3Enum paymentType,
    final Double page,
    final Double limit)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `startDate` | `String` | Query, Optional | Filter payments created on or after this ISO 8601 date. |
| `endDate` | `String` | Query, Optional | Filter payments created before this ISO 8601 date. |
| `paymentType` | [`PaymentType3Enum`](../../doc/models/payment-type-3-enum.md) | Query, Optional | Filter payments by type ('withdrawal', 'deposit', 'onramp', 'offramp', 'payment', 'transfer'). |
| `page` | `Double` | Query, Optional | Page number for pagination (1-based). |
| `limit` | `Double` | Query, Optional | Number of items per page. |

## Response Type

[`PaymentListResponse`](../../doc/models/payment-list-response.md)

## Example Usage

```java
String authorization = "Bearer <token>";

paymentsController.getPaymentsAsync(authorization, null, null, null, null, null).thenAccept(result -> {
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


# Create Payment

Create a payment. Returns the created payment details.

```java
CompletableFuture<PaymentResponse> createPaymentAsync(
    final String authorization,
    final CreatePaymentRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`CreatePaymentRequest`](../../doc/models/create-payment-request.md) | Body, Required | - |

## Response Type

[`PaymentResponse`](../../doc/models/payment-response.md)

## Example Usage

```java
String authorization = "Bearer <token>";
CreatePaymentRequest body = new CreatePaymentRequest.Builder(
    "USDC",
    "USDC"
)
.fromAmount("0.01")
.toAmount("0.01")
.fromNetwork("POLYGON")
.toNetwork("POLYGON")
.organizationReferenceId("ref_123")
.originatorAccountId("2113b166-5873-42fd-85fe-5b1a02940d43")
.sourceAccountId("6de8a7e9-be79-4885-9b65-b25b11d38078")
.beneficiaryAccountId("53b7aabd-97bc-4a4f-9f9c-1c1c69474889")
.build();

paymentsController.createPaymentAsync(authorization, body).thenAccept(result -> {
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


# Get Payment by Id

Retrieve a specific payment by ID.

```java
CompletableFuture<PaymentResponse> getPaymentByIdAsync(
    final String paymentId,
    final String authorization)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paymentId` | `String` | Template, Required | - |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |

## Response Type

[`PaymentResponse`](../../doc/models/payment-response.md)

## Example Usage

```java
String paymentId = "paymentId2";
String authorization = "Bearer <token>";

paymentsController.getPaymentByIdAsync(paymentId, authorization).thenAccept(result -> {
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


# Update Payment

Update a payment with accounts.

```java
CompletableFuture<PaymentResponse> updatePaymentAsync(
    final String paymentId,
    final String authorization,
    final UpdatePaymentRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paymentId` | `String` | Template, Required | - |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`UpdatePaymentRequest`](../../doc/models/update-payment-request.md) | Body, Required | - |

## Response Type

[`PaymentResponse`](../../doc/models/payment-response.md)

## Example Usage

```java
String paymentId = "paymentId2";
String authorization = "Bearer <token>";
UpdatePaymentRequest body = new UpdatePaymentRequest.Builder(
    "2113b166-5873-42fd-85fe-5b1a02940d43",
    "6de8a7e9-be79-4885-9b65-b25b11d38078",
    "53b7aabd-97bc-4a4f-9f9c-1c1c69474889"
)
.organizationReferenceId("ref_456")
.build();

paymentsController.updatePaymentAsync(paymentId, authorization, body).thenAccept(result -> {
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


# Review Payment

Manually review and approve or reject a payment requiring risk review.

```java
CompletableFuture<PaymentResponse> reviewPaymentAsync(
    final UUID paymentId,
    final String authorization,
    final ReviewPaymentRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paymentId` | `UUID` | Template, Required | Unique identifier of the payment to review |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`ReviewPaymentRequest`](../../doc/models/review-payment-request.md) | Body, Required | - |

## Response Type

[`PaymentResponse`](../../doc/models/payment-response.md)

## Example Usage

```java
UUID paymentId = UUID.fromString("5a9c3e7f-2b1d-4f48-a6e0-8c4b2d1f9a3e");
String authorization = "Bearer <token>";
ReviewPaymentRequest body = new ReviewPaymentRequest.Builder(
    true
)
.build();

paymentsController.reviewPaymentAsync(paymentId, authorization, body).thenAccept(result -> {
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

