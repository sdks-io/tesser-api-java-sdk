
# Tenant Api Credentials

## Structure

`TenantApiCredentials`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ClientId` | `String` | Required | Auth0 M2M Client ID | String getClientId() | setClientId(String clientId) |
| `ClientSecret` | `String` | Required | Auth0 M2M Client Secret (only shown once!) | String getClientSecret() | setClientSecret(String clientSecret) |
| `TokenEndpoint` | `String` | Required | Auth0 token endpoint URL | String getTokenEndpoint() | setTokenEndpoint(String tokenEndpoint) |
| `Audience` | `String` | Required | API audience for token requests | String getAudience() | setAudience(String audience) |

## Example (as JSON)

```json
{
  "client_id": "client_id8",
  "client_secret": "client_secret4",
  "token_endpoint": "token_endpoint8",
  "audience": "audience2"
}
```

