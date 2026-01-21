# Currencies

```java
CurrenciesController currenciesController = client.getCurrenciesController();
```

## Class Name

`CurrenciesController`


# Get Currencies

Retrieve list of all supported currencies (crypto and fiat). Returns an array with currency name, key, decimals, and network information.

```java
CompletableFuture<List<Currency>> getCurrenciesAsync(
    final String authorization)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `String` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |

## Response Type

[`List<Currency>`](../../doc/models/currency.md)

## Example Usage

```java
String authorization = "Bearer <token>";

currenciesController.getCurrenciesAsync(authorization).thenAccept(result -> {
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

