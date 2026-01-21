# Accounts

```java
AccountsController accountsController = client.getAccountsController();
```

## Class Name

`AccountsController`

## Methods

* [Find All](../../doc/controllers/accounts.md#find-all)
* [Create Bank](../../doc/controllers/accounts.md#create-bank)
* [Create Wallet](../../doc/controllers/accounts.md#create-wallet)
* [Find One 2](../../doc/controllers/accounts.md#find-one-2)
* [Update](../../doc/controllers/accounts.md#update)


# Find All

Retrieve all accounts (both bank and wallet accounts) for your workspace.

```java
CompletableFuture<AccountListResponse> findAllAsync(
    final String authorization,
    final Type4Enum type,
    final String tenantId,
    final String counterpartyId,
    final Boolean includeSensitive)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `type` | [`Type4Enum`](../../doc/models/type-4-enum.md) | Query, Optional | Filter by account type |
| `tenantId` | `String` | Query, Optional | Filter by tenant ID. At most one of tenant_id or counterparty_id may be provided. |
| `counterpartyId` | `String` | Query, Optional | Filter by counterparty ID. At most one of tenant_id or counterparty_id may be provided. |
| `includeSensitive` | `Boolean` | Query, Optional | If true, includes sensitive fields like bank_account_number. |

## Response Type

[`AccountListResponse`](../../doc/models/account-list-response.md)

## Example Usage

```java
String authorization = "Bearer <token>";

accountsController.findAllAsync(authorization, null, null, null, null).thenAccept(result -> {
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


# Create Bank

Create a new fiat bank account.

```java
CompletableFuture<CreateBankResponse> createBankAsync(
    final String authorization,
    final CreateBankRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`CreateBankRequest`](../../doc/models/create-bank-request.md) | Body, Required | Bank account details |

## Response Type

[`CreateBankResponse`](../../doc/models/create-bank-response.md)

## Example Usage

```java
String authorization = "Bearer <token>";
CreateBankRequest body = new CreateBankRequest.Builder(
    "Operating Account - EU",
    "Chase Bank",
    "SWIFT",
    "CHASUS33",
    "123456789"
)
.counterpartyId("2a7e1c9f-4b3d-4a82-b6e0-8f5c2d1a9b3e")
.build();

accountsController.createBankAsync(authorization, body).thenAccept(result -> {
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


# Create Wallet

Create a new stablecoin wallet account.

```java
CompletableFuture<CreateWalletResponse> createWalletAsync(
    final String authorization,
    final CreateWalletRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`CreateWalletRequest`](../../doc/models/create-wallet-request.md) | Body, Required | Wallet account details |

## Response Type

[`CreateWalletResponse`](../../doc/models/create-wallet-response.md)

## Example Usage

```java
String authorization = "Bearer <token>";
CreateWalletRequest body = new CreateWalletRequest.Builder(
    "b53f6690-3242-4942-9907-885779632832",
    "Treasury Wallet (Omnibus)",
    Type3Enum.STABLECOIN_ETHEREUM,
    "eyJwdWJsaWNLZXkiOiJwdWJfZXhhbXBsZSIsInNpZ25hdHVyZSI6InNpZ19leGFtcGxlIiwic2NoZW1lIjoiRUQyNTUxOSJ9"
)
.build();

accountsController.createWalletAsync(authorization, body).thenAccept(result -> {
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


# Find One 2

Retrieve a specific account (wallet or bank) by its unique identifier

```java
CompletableFuture<AccountResponse> findOne2Async(
    final String id,
    final String authorization,
    final Boolean includeSensitive)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Account ID (UUID) |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `includeSensitive` | `Boolean` | Query, Optional | If true, includes sensitive fields like bank_account_number. |

## Response Type

[`AccountResponse`](../../doc/models/account-response.md)

## Example Usage

```java
String id = "7a3d8f2e-6b4c-4a91-b8e5-2f9c1d7e3a0b";
String authorization = "Bearer <token>";

accountsController.findOne2Async(id, authorization, null).thenAccept(result -> {
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


# Update

Update an existing account's information.

```java
CompletableFuture<UpdateAccountResponse> updateAsync(
    final String id,
    final String authorization,
    final UpdateAccountRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | Account ID (UUID) |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`UpdateAccountRequest`](../../doc/models/update-account-request.md) | Body, Required | - |

## Response Type

[`UpdateAccountResponse`](../../doc/models/update-account-response.md)

## Example Usage

```java
String id = "7a3d8f2e-6b4c-4a91-b8e5-2f9c1d7e3a0b";
String authorization = "Bearer <token>";
UpdateAccountRequest body = new UpdateAccountRequest.Builder()
    .name("Updated Treasury Wallet")
    .build();

accountsController.updateAsync(id, authorization, body).thenAccept(result -> {
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

