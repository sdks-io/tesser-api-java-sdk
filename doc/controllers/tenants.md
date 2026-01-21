# Tenants

```java
TenantsController tenantsController = client.getTenantsController();
```

## Class Name

`TenantsController`

## Methods

* [Create 1](../../doc/controllers/tenants.md#create-1)
* [Find All 2](../../doc/controllers/tenants.md#find-all-2)
* [Find One 1](../../doc/controllers/tenants.md#find-one-1)
* [Update 2](../../doc/controllers/tenants.md#update-2)


# Create 1

Create a new tenant for your workspace. Tenants are business customers that integrate via APIs.

```java
CompletableFuture<CreateTenantResponse> create1Async(
    final String authorization,
    final CreateTenantRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`CreateTenantRequest`](../../doc/models/create-tenant-request.md) | Body, Required | - |

## Response Type

[`CreateTenantResponse`](../../doc/models/create-tenant-response.md)

## Example Usage

```java
String authorization = "Bearer <token>";
CreateTenantRequest body = new CreateTenantRequest.Builder(
    "Acme Corporation"
)
.businessDba(CreateTenantRequestBusinessDba.fromString(
        "Acme Co"
    ))
.businessAddressCountry(CreateTenantRequestBusinessAddressCountry.fromString(
        "US"
    ))
.businessStreetAddress1(CreateTenantRequestBusinessStreetAddress1.fromString(
        "123 Corp Blvd"
    ))
.businessStreetAddress2(CreateTenantRequestBusinessStreetAddress2.fromString(
        "Suite 100"
    ))
.businessCity(CreateTenantRequestBusinessCity.fromString(
        "New York"
    ))
.businessState(CreateTenantRequestBusinessState.fromString(
        "NY"
    ))
.businessLegalEntityIdentifier(CreateTenantRequestBusinessLegalEntityIdentifier.fromString(
        "123456789"
    ))
.webhookUrl(CreateTenantRequestWebhookUrl.fromString(
        "https://example.com/webhooks/tesser"
    ))
.build();

tenantsController.create1Async(authorization, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": {
    "id": "4e8c2a6f-1b9d-4f37-a5e0-7c3b8d2f1a9e",
    "workspace_id": "b53f6690-3242-4942-9907-885779632832",
    "business_legal_name": "Acme Corporation",
    "business_dba": "Acme Co",
    "business_address_country": "US",
    "business_street_address1": "123 Corp Blvd",
    "business_street_address2": "Suite 100",
    "business_city": "New York",
    "business_state": "NY",
    "business_legal_entity_identifier": "9876543210",
    "country": "US",
    "webhook_url": "https://acme.com/webhooks/tesser",
    "created_at": "2024-01-15T10:30:00.000Z",
    "updated_at": "2024-01-15T10:30:00.000Z"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Details coming soon | `ApiException` |


# Find All 2

Retrieve all tenants for your workspace with optional search filtering.

```java
CompletableFuture<TenantListResponse> findAll2Async(
    final String authorization,
    final Boolean includeSecure)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `includeSecure` | `Boolean` | Query, Optional | Include secure fields (PII) |

## Response Type

[`TenantListResponse`](../../doc/models/tenant-list-response.md)

## Example Usage

```java
String authorization = "Bearer <token>";

tenantsController.findAll2Async(authorization, null).thenAccept(result -> {
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


# Find One 1

Retrieve a specific tenant by its unique identifier

```java
CompletableFuture<TenantResponse> findOne1Async(
    final String id,
    final String authorization,
    final Boolean includeSecure)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Tenant ID (UUID) |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `includeSecure` | `Boolean` | Query, Optional | Include secure fields (PII) |

## Response Type

[`TenantResponse`](../../doc/models/tenant-response.md)

## Example Usage

```java
String id = "4e8c2a6f-1b9d-4f37-a5e0-7c3b8d2f1a9e";
String authorization = "Bearer <token>";

tenantsController.findOne1Async(id, authorization, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": {
    "id": "4e8c2a6f-1b9d-4f37-a5e0-7c3b8d2f1a9e",
    "workspace_id": "b53f6690-3242-4942-9907-885779632832",
    "business_legal_name": "Acme Corporation",
    "business_dba": "Acme Co",
    "business_address_country": "US",
    "business_street_address1": "123 Corp Blvd",
    "business_street_address2": "Suite 100",
    "business_city": "New York",
    "business_state": "NY",
    "business_legal_entity_identifier": "9876543210",
    "country": "US",
    "webhook_url": "https://acme.com/webhooks/tesser",
    "created_at": "2024-01-15T10:30:00.000Z",
    "updated_at": "2024-01-15T10:30:00.000Z"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Details coming soon | `ApiException` |


# Update 2

Update an existing tenant's information.

Only the following fields can be updated:

- business_legal_name
- business_dba
- business_address_country
- webhook_url

At least one field must be provided.

```java
CompletableFuture<UpdateTenantResponse> update2Async(
    final String id,
    final String authorization,
    final UpdateTenantRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Tenant ID (UUID) |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`UpdateTenantRequest`](../../doc/models/update-tenant-request.md) | Body, Required | - |

## Response Type

[`UpdateTenantResponse`](../../doc/models/update-tenant-response.md)

## Example Usage

```java
String id = "4e8c2a6f-1b9d-4f37-a5e0-7c3b8d2f1a9e";
String authorization = "Bearer <token>";
UpdateTenantRequest body = new UpdateTenantRequest.Builder()
    .businessDba(UpdateTenantRequestBusinessDba.fromString(
        "Acme Corp Updated"
    ))
    .webhookUrl(UpdateTenantRequestWebhookUrl.fromString(
        "https://acme.com/webhooks/tesser"
    ))
    .build();

tenantsController.update2Async(id, authorization, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "data": {
    "id": "4e8c2a6f-1b9d-4f37-a5e0-7c3b8d2f1a9e",
    "workspace_id": "b53f6690-3242-4942-9907-885779632832",
    "business_legal_name": "Acme Corporation",
    "business_dba": "Acme Corp Updated",
    "business_address_country": "US",
    "business_street_address1": "123 Corp Blvd",
    "business_street_address2": "Suite 100",
    "business_city": "New York",
    "business_state": "NY",
    "business_legal_entity_identifier": "9876543210",
    "country": "US",
    "webhook_url": "https://acme.com/webhooks/tesser",
    "created_at": "2024-01-15T10:30:00.000Z",
    "updated_at": "2024-03-01T12:00:00.000Z"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Details coming soon | `ApiException` |

