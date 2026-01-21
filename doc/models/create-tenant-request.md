
# Create Tenant Request

## Structure

`CreateTenantRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BusinessLegalName` | `String` | Required | Legal name of the business tenant.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | String getBusinessLegalName() | setBusinessLegalName(String businessLegalName) |
| `BusinessDba` | [`CreateTenantRequestBusinessDba`](../../doc/models/containers/create-tenant-request-business-dba.md) | Optional | This is a container for any-of cases. | CreateTenantRequestBusinessDba getBusinessDba() | setBusinessDba(CreateTenantRequestBusinessDba businessDba) |
| `BusinessAddressCountry` | [`CreateTenantRequestBusinessAddressCountry`](../../doc/models/containers/create-tenant-request-business-address-country.md) | Optional | This is a container for any-of cases. | CreateTenantRequestBusinessAddressCountry getBusinessAddressCountry() | setBusinessAddressCountry(CreateTenantRequestBusinessAddressCountry businessAddressCountry) |
| `BusinessStreetAddress1` | [`CreateTenantRequestBusinessStreetAddress1`](../../doc/models/containers/create-tenant-request-business-street-address-1.md) | Optional | This is a container for any-of cases. | CreateTenantRequestBusinessStreetAddress1 getBusinessStreetAddress1() | setBusinessStreetAddress1(CreateTenantRequestBusinessStreetAddress1 businessStreetAddress1) |
| `BusinessStreetAddress2` | [`CreateTenantRequestBusinessStreetAddress2`](../../doc/models/containers/create-tenant-request-business-street-address-2.md) | Optional | This is a container for any-of cases. | CreateTenantRequestBusinessStreetAddress2 getBusinessStreetAddress2() | setBusinessStreetAddress2(CreateTenantRequestBusinessStreetAddress2 businessStreetAddress2) |
| `BusinessCity` | [`CreateTenantRequestBusinessCity`](../../doc/models/containers/create-tenant-request-business-city.md) | Optional | This is a container for any-of cases. | CreateTenantRequestBusinessCity getBusinessCity() | setBusinessCity(CreateTenantRequestBusinessCity businessCity) |
| `BusinessState` | [`CreateTenantRequestBusinessState`](../../doc/models/containers/create-tenant-request-business-state.md) | Optional | This is a container for any-of cases. | CreateTenantRequestBusinessState getBusinessState() | setBusinessState(CreateTenantRequestBusinessState businessState) |
| `BusinessLegalEntityIdentifier` | [`CreateTenantRequestBusinessLegalEntityIdentifier`](../../doc/models/containers/create-tenant-request-business-legal-entity-identifier.md) | Optional | This is a container for any-of cases. | CreateTenantRequestBusinessLegalEntityIdentifier getBusinessLegalEntityIdentifier() | setBusinessLegalEntityIdentifier(CreateTenantRequestBusinessLegalEntityIdentifier businessLegalEntityIdentifier) |
| `WebhookUrl` | [`CreateTenantRequestWebhookUrl`](../../doc/models/containers/create-tenant-request-webhook-url.md) | Optional | This is a container for any-of cases. | CreateTenantRequestWebhookUrl getWebhookUrl() | setWebhookUrl(CreateTenantRequestWebhookUrl webhookUrl) |

## Example (as JSON)

```json
{
  "business_legal_name": "business_legal_name2",
  "webhook_url": "https://acme.com/webhooks/tesser",
  "business_dba": "String3",
  "business_address_country": "String9",
  "business_street_address1": "String3",
  "business_street_address2": "String7",
  "business_city": "String9"
}
```

