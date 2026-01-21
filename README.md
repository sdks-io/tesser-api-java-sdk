
# Getting Started with Tesser API (v1)

## Introduction

The Tesser Payments Platform API documentation (v1)

## Install the Package

Install the SDK by adding the following dependency in your project's pom.xml file:

```xml
<dependency>
  <groupId>io.sdks</groupId>
  <artifactId>tesser-api-sdk</artifactId>
  <version>1.0.5</version>
</dependency>
```

You can also view the package at:
https://central.sonatype.com/artifact/io.sdks/tesser-api-sdk/1.0.5

## Test the SDK

The generated code and the server can be tested using automatically generated test cases.
JUnit is used as the testing framework and test runner.

In Eclipse, for running the tests do the following:

1. Select the project TesserAPIV1Lib from the package explorer.
2. Select `Run -> Run as -> JUnit Test` or use `Alt + Shift + X` followed by `T` to run the Tests.

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| httpClientConfig | [`Consumer<HttpClientConfiguration.Builder>`](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/http-client-configuration-builder.md) | Set up Http Client Configuration instance. |
| bearerAuthCredentials | [`BearerAuthCredentials`](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/auth/oauth-2-bearer-token.md) | The Credentials Setter for OAuth 2 Bearer token |

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

## Authorization

This API uses the following authentication schemes.

* [`bearer (OAuth 2 Bearer token)`](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/auth/oauth-2-bearer-token.md)

## List of APIs

* [Payments](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/controllers/payments.md)
* [Health](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/controllers/health.md)
* [Accounts](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/controllers/accounts.md)
* [Currencies](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/controllers/currencies.md)
* [Counterparties](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/controllers/counterparties.md)
* [Tenants](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/controllers/tenants.md)
* [Networks](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/controllers/networks.md)
* [Experimental](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/controllers/experimental.md)
* [Treasury](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/controllers/treasury.md)

## SDK Infrastructure

### Configuration

* [Configuration Interface](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/configuration-interface.md)
* [HttpClientConfiguration](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/http-client-configuration.md)
* [HttpClientConfiguration.Builder](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/http-client-configuration-builder.md)
* [HttpProxyConfiguration](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/http-proxy-configuration.md)
* [HttpProxyConfiguration.Builder](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/http-proxy-configuration-builder.md)

### HTTP

* [Headers](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/headers.md)
* [HttpCallback Interface](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/http-callback-interface.md)
* [HttpContext](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/http-context.md)
* [HttpBodyRequest](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/http-body-request.md)
* [HttpRequest](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/http-request.md)
* [HttpResponse](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/http-response.md)
* [HttpStringResponse](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/http-string-response.md)

### Utilities

* [ApiException](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/api-exception.md)
* [ApiHelper](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/api-helper.md)
* [FileWrapper](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/file-wrapper.md)
* [DateTimeHelper](https://www.github.com/sdks-io/tesser-api-java-sdk/tree/1.0.5/doc/date-time-helper.md)

