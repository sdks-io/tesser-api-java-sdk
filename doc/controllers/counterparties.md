# Counterparties

```java
CounterpartiesController counterpartiesController = client.getCounterpartiesController();
```

## Class Name

`CounterpartiesController`

## Methods

* [Create](../../doc/controllers/counterparties.md#create)
* [Find All 1](../../doc/controllers/counterparties.md#find-all-1)
* [Find One](../../doc/controllers/counterparties.md#find-one)
* [Update 1](../../doc/controllers/counterparties.md#update-1)


# Create

Create a new counterparty for your workspace.

A counterparty is any external party that your organization transacts with,
such as vendors, customers, or partners.

**Classifications:**

- **individual**: A natural person (requires first/last name)
- **business**: A legal entity (requires legal name)

```java
CompletableFuture<CreateCounterpartyResponse> createAsync(
    final String authorization,
    final CreateCounterpartyRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`CreateCounterpartyRequest`](../../doc/models/create-counterparty-request.md) | Body, Required | - |

## Response Type

[`CreateCounterpartyResponse`](../../doc/models/create-counterparty-response.md)

## Example Usage

```java
String authorization = "Bearer <token>";
CreateCounterpartyRequest body = new CreateCounterpartyRequest.Builder(
    ClassificationEnum.INDIVIDUAL
)
.individualFirstName(CreateCounterpartyRequestIndividualFirstName.fromString(
        "John"
    ))
.individualLastName(CreateCounterpartyRequestIndividualLastName.fromString(
        "Doe"
    ))
.individualAddressCountry(CreateCounterpartyRequestIndividualAddressCountry.fromString(
        "US"
    ))
.individualDateOfBirth(CreateCounterpartyRequestIndividualDateOfBirth.fromString(
        "1980-01-01"
    ))
.individualNationalIdentificationNumber(CreateCounterpartyRequestIndividualNationalIdentificationNumber.fromString(
        "123456789"
    ))
.individualStreetAddress1(CreateCounterpartyRequestIndividualStreetAddress1.fromString(
        "123 Main St"
    ))
.individualStreetAddress2(CreateCounterpartyRequestIndividualStreetAddress2.fromString(
        "Apt 4B"
    ))
.individualCity(CreateCounterpartyRequestIndividualCity.fromString(
        "New York"
    ))
.individualState(CreateCounterpartyRequestIndividualState.fromString(
        "NY"
    ))
.individualPostalCode(CreateCounterpartyRequestIndividualPostalCode.fromString(
        "10001"
    ))
.build();

counterpartiesController.createAsync(authorization, body).thenAccept(result -> {
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


# Find All 1

Retrieve all counterparties for your workspace with optional filtering.

Use query parameters to filter results:

- **classification**: Filter by 'individual' or 'business'

```java
CompletableFuture<CounterpartyListResponse> findAll1Async(
    final String authorization,
    final Classification7Enum classification,
    final Boolean includeSecure)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `classification` | [`Classification7Enum`](../../doc/models/classification-7-enum.md) | Query, Optional | Filter by classification |
| `includeSecure` | `Boolean` | Query, Optional | Include secure fields (PII) |

## Response Type

[`CounterpartyListResponse`](../../doc/models/counterparty-list-response.md)

## Example Usage

```java
String authorization = "Bearer <token>";

counterpartiesController.findAll1Async(authorization, null, null).thenAccept(result -> {
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


# Find One

Retrieve a specific counterparty by its unique identifier

```java
CompletableFuture<CounterpartyResponse> findOneAsync(
    final String id,
    final String authorization,
    final Classification7Enum classification,
    final Boolean includeSecure)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Counterparty ID (UUID) |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `classification` | [`Classification7Enum`](../../doc/models/classification-7-enum.md) | Query, Optional | Filter by classification ('individual' or 'business'). |
| `includeSecure` | `Boolean` | Query, Optional | Include secure fields (PII) |

## Response Type

[`CounterpartyResponse`](../../doc/models/counterparty-response.md)

## Example Usage

```java
String id = "3e9a7c2f-1b8d-4e56-a0f3-5c2d8b1e9a7f";
String authorization = "Bearer <token>";

counterpartiesController.findOneAsync(id, authorization, null, null).thenAccept(result -> {
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


# Update 1

Update an existing counterparty's information.

Only provide the fields you want to update. At least one field must be provided.

**Note:** If changing classification from 'individual' to 'business' (or vice versa),
make sure to also provide the appropriate fields for the new classification.

```java
CompletableFuture<UpdateCounterpartyResponse> update1Async(
    final String id,
    final String authorization,
    final UpdateCounterpartyRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Counterparty ID (UUID) |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`UpdateCounterpartyRequest`](../../doc/models/update-counterparty-request.md) | Body, Required | - |

## Response Type

[`UpdateCounterpartyResponse`](../../doc/models/update-counterparty-response.md)

## Example Usage

```java
String id = "3e9a7c2f-1b8d-4e56-a0f3-5c2d8b1e9a7f";
String authorization = "Bearer <token>";
UpdateCounterpartyRequest body = new UpdateCounterpartyRequest.Builder()
    .build();

counterpartiesController.update1Async(id, authorization, body).thenAccept(result -> {
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

