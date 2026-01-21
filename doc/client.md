
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| httpClientConfig | [`Consumer<HttpClientConfiguration.Builder>`](../doc/http-client-configuration-builder.md) | Set up Http Client Configuration instance. |
| bearerAuthCredentials | [`BearerAuthCredentials`](auth/oauth-2-bearer-token.md) | The Credentials Setter for OAuth 2 Bearer token |

The API client can be initialized as follows:

```java
import app.zuplo.tesserplatformv1pull51me98e48a7.TesserAPIV1Client;
import app.zuplo.tesserplatformv1pull51me98e48a7.authentication.BearerAuthModel;
import app.zuplo.tesserplatformv1pull51me98e48a7.exceptions.ApiException;
import java.io.IOException;

public class Program {
    public static void main(String[] args) {
        TesserAPIV1Client client = new TesserAPIV1Client.Builder()
            .httpClientConfig(configBuilder -> configBuilder
                    .timeout(0))
            .bearerAuthCredentials(new BearerAuthModel.Builder(
                    "AccessToken"
                )
                .build())
            .build();

    }
}
```

## Tesser API (v1)Client Class

The gateway for the SDK. This class acts as a factory for the Controllers and also holds the configuration of the SDK.

### Controllers

| Name | Description | Return Type |
|  --- | --- | --- |
| `getPaymentsController()` | Provides access to Payments controller. | `PaymentsController` |
| `getHealthController()` | Provides access to Health controller. | `HealthController` |
| `getAccountsController()` | Provides access to Accounts controller. | `AccountsController` |
| `getCurrenciesController()` | Provides access to Currencies controller. | `CurrenciesController` |
| `getCounterpartiesController()` | Provides access to Counterparties controller. | `CounterpartiesController` |
| `getTenantsController()` | Provides access to Tenants controller. | `TenantsController` |
| `getNetworksController()` | Provides access to Networks controller. | `NetworksController` |
| `getExperimentalController()` | Provides access to Experimental controller. | `ExperimentalController` |
| `getTreasuryController()` | Provides access to Treasury controller. | `TreasuryController` |

### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `shutdown()` | Shutdown the underlying HttpClient instance. | `void` |
| `getEnvironment()` | Current API environment. | `Environment` |
| `getHttpClient()` | The HTTP Client instance to use for making HTTP requests. | `HttpClient` |
| `getHttpClientConfig()` | Http Client Configuration instance. | [`ReadonlyHttpClientConfiguration`](../doc/http-client-configuration.md) |
| `getBearerAuthCredentials()` | The credentials to use with BearerAuth. | [`BearerAuthCredentials`](auth/oauth-2-bearer-token.md) |
| `getBaseUri(Server server)` | Get base URI by current environment | `String` |
| `getBaseUri()` | Get base URI by current environment | `String` |

