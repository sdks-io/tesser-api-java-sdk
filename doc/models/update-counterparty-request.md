
# Update Counterparty Request

## Structure

`UpdateCounterpartyRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Classification` | [`ClassificationEnum`](../../doc/models/classification-enum.md) | Optional | Classification: 'individual' or 'business'. | ClassificationEnum getClassification() | setClassification(ClassificationEnum classification) |
| `TenantId` | [`UpdateCounterpartyRequestTenantId`](../../doc/models/containers/update-counterparty-request-tenant-id.md) | Optional | This is a container for any-of cases. | UpdateCounterpartyRequestTenantId getTenantId() | setTenantId(UpdateCounterpartyRequestTenantId tenantId) |
| `IndividualFirstName` | [`UpdateCounterpartyRequestIndividualFirstName`](../../doc/models/containers/update-counterparty-request-individual-first-name.md) | Optional | This is a container for any-of cases. | UpdateCounterpartyRequestIndividualFirstName getIndividualFirstName() | setIndividualFirstName(UpdateCounterpartyRequestIndividualFirstName individualFirstName) |
| `IndividualLastName` | [`UpdateCounterpartyRequestIndividualLastName`](../../doc/models/containers/update-counterparty-request-individual-last-name.md) | Optional | This is a container for any-of cases. | UpdateCounterpartyRequestIndividualLastName getIndividualLastName() | setIndividualLastName(UpdateCounterpartyRequestIndividualLastName individualLastName) |
| `IndividualAddressCountry` | [`UpdateCounterpartyRequestIndividualAddressCountry`](../../doc/models/containers/update-counterparty-request-individual-address-country.md) | Optional | This is a container for any-of cases. | UpdateCounterpartyRequestIndividualAddressCountry getIndividualAddressCountry() | setIndividualAddressCountry(UpdateCounterpartyRequestIndividualAddressCountry individualAddressCountry) |
| `BusinessLegalName` | [`UpdateCounterpartyRequestBusinessLegalName`](../../doc/models/containers/update-counterparty-request-business-legal-name.md) | Optional | This is a container for any-of cases. | UpdateCounterpartyRequestBusinessLegalName getBusinessLegalName() | setBusinessLegalName(UpdateCounterpartyRequestBusinessLegalName businessLegalName) |
| `BusinessDba` | [`UpdateCounterpartyRequestBusinessDba`](../../doc/models/containers/update-counterparty-request-business-dba.md) | Optional | This is a container for any-of cases. | UpdateCounterpartyRequestBusinessDba getBusinessDba() | setBusinessDba(UpdateCounterpartyRequestBusinessDba businessDba) |
| `BusinessAddressCountry` | [`UpdateCounterpartyRequestBusinessAddressCountry`](../../doc/models/containers/update-counterparty-request-business-address-country.md) | Optional | This is a container for any-of cases. | UpdateCounterpartyRequestBusinessAddressCountry getBusinessAddressCountry() | setBusinessAddressCountry(UpdateCounterpartyRequestBusinessAddressCountry businessAddressCountry) |

## Example (as JSON)

```json
{
  "classification": "individual",
  "tenant_id": "00001eca-0000-0000-0000-000000000000",
  "individual_first_name": "String1",
  "individual_last_name": "String5",
  "individual_address_country": "String1"
}
```

