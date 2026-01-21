
# Update Tenant Request

## Structure

`UpdateTenantRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BusinessLegalName` | `String` | Optional | Updated legal business name.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | String getBusinessLegalName() | setBusinessLegalName(String businessLegalName) |
| `BusinessDba` | [`UpdateTenantRequestBusinessDba`](../../doc/models/containers/update-tenant-request-business-dba.md) | Optional | This is a container for any-of cases. | UpdateTenantRequestBusinessDba getBusinessDba() | setBusinessDba(UpdateTenantRequestBusinessDba businessDba) |
| `BusinessAddressCountry` | [`UpdateTenantRequestBusinessAddressCountry`](../../doc/models/containers/update-tenant-request-business-address-country.md) | Optional | This is a container for any-of cases. | UpdateTenantRequestBusinessAddressCountry getBusinessAddressCountry() | setBusinessAddressCountry(UpdateTenantRequestBusinessAddressCountry businessAddressCountry) |
| `WebhookUrl` | [`UpdateTenantRequestWebhookUrl`](../../doc/models/containers/update-tenant-request-webhook-url.md) | Optional | This is a container for any-of cases. | UpdateTenantRequestWebhookUrl getWebhookUrl() | setWebhookUrl(UpdateTenantRequestWebhookUrl webhookUrl) |

## Example (as JSON)

```json
{
  "business_legal_name": "business_legal_name0",
  "business_dba": "String1",
  "business_address_country": "String7",
  "webhook_url": "String7"
}
```

