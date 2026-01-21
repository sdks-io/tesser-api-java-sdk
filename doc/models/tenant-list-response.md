
# Tenant List Response

## Structure

`TenantListResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`List<Tenant>`](../../doc/models/tenant.md) | Required | List of tenants | List<Tenant> getData() | setData(List<Tenant> data) |

## Example (as JSON)

```json
{
  "data": [
    {
      "id": "id0",
      "workspace_id": "workspace_id2",
      "business_legal_name": "String5",
      "business_dba": "String5",
      "business_address_country": "String9",
      "business_street_address1": "String5",
      "business_street_address2": "String3",
      "business_city": "String9",
      "business_state": "String7",
      "business_legal_entity_identifier": "String3",
      "country": "String5",
      "webhook_url": "String9",
      "created_at": "created_at8",
      "updated_at": "updated_at6"
    }
  ]
}
```

