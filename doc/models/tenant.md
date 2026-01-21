
# Tenant

## Structure

`Tenant`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Unique identifier for the tenant | String getId() | setId(String id) |
| `WorkspaceId` | `String` | Required | Workspace ID the tenant belongs to | String getWorkspaceId() | setWorkspaceId(String workspaceId) |
| `BusinessLegalName` | [`TenantBusinessLegalName`](../../doc/models/containers/tenant-business-legal-name.md) | Required | This is a container for any-of cases. | TenantBusinessLegalName getBusinessLegalName() | setBusinessLegalName(TenantBusinessLegalName businessLegalName) |
| `BusinessDba` | [`TenantBusinessDba`](../../doc/models/containers/tenant-business-dba.md) | Required | This is a container for any-of cases. | TenantBusinessDba getBusinessDba() | setBusinessDba(TenantBusinessDba businessDba) |
| `BusinessAddressCountry` | [`TenantBusinessAddressCountry`](../../doc/models/containers/tenant-business-address-country.md) | Required | This is a container for any-of cases. | TenantBusinessAddressCountry getBusinessAddressCountry() | setBusinessAddressCountry(TenantBusinessAddressCountry businessAddressCountry) |
| `BusinessStreetAddress1` | [`TenantBusinessStreetAddress1`](../../doc/models/containers/tenant-business-street-address-1.md) | Required | This is a container for any-of cases. | TenantBusinessStreetAddress1 getBusinessStreetAddress1() | setBusinessStreetAddress1(TenantBusinessStreetAddress1 businessStreetAddress1) |
| `BusinessStreetAddress2` | [`TenantBusinessStreetAddress2`](../../doc/models/containers/tenant-business-street-address-2.md) | Required | This is a container for any-of cases. | TenantBusinessStreetAddress2 getBusinessStreetAddress2() | setBusinessStreetAddress2(TenantBusinessStreetAddress2 businessStreetAddress2) |
| `BusinessCity` | [`TenantBusinessCity`](../../doc/models/containers/tenant-business-city.md) | Required | This is a container for any-of cases. | TenantBusinessCity getBusinessCity() | setBusinessCity(TenantBusinessCity businessCity) |
| `BusinessState` | [`TenantBusinessState`](../../doc/models/containers/tenant-business-state.md) | Required | This is a container for any-of cases. | TenantBusinessState getBusinessState() | setBusinessState(TenantBusinessState businessState) |
| `BusinessLegalEntityIdentifier` | [`TenantBusinessLegalEntityIdentifier`](../../doc/models/containers/tenant-business-legal-entity-identifier.md) | Required | This is a container for any-of cases. | TenantBusinessLegalEntityIdentifier getBusinessLegalEntityIdentifier() | setBusinessLegalEntityIdentifier(TenantBusinessLegalEntityIdentifier businessLegalEntityIdentifier) |
| `Country` | [`TenantCountry`](../../doc/models/containers/tenant-country.md) | Required | This is a container for any-of cases. | TenantCountry getCountry() | setCountry(TenantCountry country) |
| `WebhookUrl` | [`TenantWebhookUrl`](../../doc/models/containers/tenant-webhook-url.md) | Required | This is a container for any-of cases. | TenantWebhookUrl getWebhookUrl() | setWebhookUrl(TenantWebhookUrl webhookUrl) |
| `CreatedAt` | `String` | Required | Creation timestamp in ISO 8601 format | String getCreatedAt() | setCreatedAt(String createdAt) |
| `UpdatedAt` | `String` | Required | Last update timestamp in ISO 8601 format | String getUpdatedAt() | setUpdatedAt(String updatedAt) |

## Example (as JSON)

```json
{
  "id": "id0",
  "workspace_id": "workspace_id2",
  "business_legal_name": "String7",
  "business_dba": "String7",
  "business_address_country": "String9",
  "business_street_address1": "String7",
  "business_street_address2": "String3",
  "business_city": "String3",
  "business_state": "String7",
  "business_legal_entity_identifier": "String3",
  "country": "String5",
  "webhook_url": "String3",
  "created_at": "created_at8",
  "updated_at": "updated_at6"
}
```

