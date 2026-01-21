
# Counterparty

## Structure

`Counterparty`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Unique identifier for the counterparty. | String getId() | setId(String id) |
| `WorkspaceId` | `String` | Required | Workspace this counterparty belongs to. | String getWorkspaceId() | setWorkspaceId(String workspaceId) |
| `Classification` | [`ClassificationEnum`](../../doc/models/classification-enum.md) | Required | Classification: 'individual' or 'business'. | ClassificationEnum getClassification() | setClassification(ClassificationEnum classification) |
| `TenantId` | [`CounterpartyTenantId`](../../doc/models/containers/counterparty-tenant-id.md) | Optional | This is a container for any-of cases. | CounterpartyTenantId getTenantId() | setTenantId(CounterpartyTenantId tenantId) |
| `IndividualFirstName` | [`CounterpartyIndividualFirstName`](../../doc/models/containers/counterparty-individual-first-name.md) | Optional | This is a container for any-of cases. | CounterpartyIndividualFirstName getIndividualFirstName() | setIndividualFirstName(CounterpartyIndividualFirstName individualFirstName) |
| `IndividualLastName` | [`CounterpartyIndividualLastName`](../../doc/models/containers/counterparty-individual-last-name.md) | Optional | This is a container for any-of cases. | CounterpartyIndividualLastName getIndividualLastName() | setIndividualLastName(CounterpartyIndividualLastName individualLastName) |
| `IndividualAddressCountry` | [`CounterpartyIndividualAddressCountry`](../../doc/models/containers/counterparty-individual-address-country.md) | Optional | This is a container for any-of cases. | CounterpartyIndividualAddressCountry getIndividualAddressCountry() | setIndividualAddressCountry(CounterpartyIndividualAddressCountry individualAddressCountry) |
| `IndividualDateOfBirth` | [`CounterpartyIndividualDateOfBirth`](../../doc/models/containers/counterparty-individual-date-of-birth.md) | Optional | This is a container for any-of cases. | CounterpartyIndividualDateOfBirth getIndividualDateOfBirth() | setIndividualDateOfBirth(CounterpartyIndividualDateOfBirth individualDateOfBirth) |
| `IndividualNationalIdentificationNumber` | [`CounterpartyIndividualNationalIdentificationNumber`](../../doc/models/containers/counterparty-individual-national-identification-number.md) | Optional | This is a container for any-of cases. | CounterpartyIndividualNationalIdentificationNumber getIndividualNationalIdentificationNumber() | setIndividualNationalIdentificationNumber(CounterpartyIndividualNationalIdentificationNumber individualNationalIdentificationNumber) |
| `IndividualStreetAddress1` | [`CounterpartyIndividualStreetAddress1`](../../doc/models/containers/counterparty-individual-street-address-1.md) | Optional | This is a container for any-of cases. | CounterpartyIndividualStreetAddress1 getIndividualStreetAddress1() | setIndividualStreetAddress1(CounterpartyIndividualStreetAddress1 individualStreetAddress1) |
| `IndividualStreetAddress2` | [`CounterpartyIndividualStreetAddress2`](../../doc/models/containers/counterparty-individual-street-address-2.md) | Optional | This is a container for any-of cases. | CounterpartyIndividualStreetAddress2 getIndividualStreetAddress2() | setIndividualStreetAddress2(CounterpartyIndividualStreetAddress2 individualStreetAddress2) |
| `IndividualCity` | [`CounterpartyIndividualCity`](../../doc/models/containers/counterparty-individual-city.md) | Optional | This is a container for any-of cases. | CounterpartyIndividualCity getIndividualCity() | setIndividualCity(CounterpartyIndividualCity individualCity) |
| `IndividualState` | [`CounterpartyIndividualState`](../../doc/models/containers/counterparty-individual-state.md) | Optional | This is a container for any-of cases. | CounterpartyIndividualState getIndividualState() | setIndividualState(CounterpartyIndividualState individualState) |
| `IndividualPostalCode` | [`CounterpartyIndividualPostalCode`](../../doc/models/containers/counterparty-individual-postal-code.md) | Optional | This is a container for any-of cases. | CounterpartyIndividualPostalCode getIndividualPostalCode() | setIndividualPostalCode(CounterpartyIndividualPostalCode individualPostalCode) |
| `BusinessLegalName` | [`CounterpartyBusinessLegalName`](../../doc/models/containers/counterparty-business-legal-name.md) | Optional | This is a container for any-of cases. | CounterpartyBusinessLegalName getBusinessLegalName() | setBusinessLegalName(CounterpartyBusinessLegalName businessLegalName) |
| `BusinessDba` | [`CounterpartyBusinessDba`](../../doc/models/containers/counterparty-business-dba.md) | Optional | This is a container for any-of cases. | CounterpartyBusinessDba getBusinessDba() | setBusinessDba(CounterpartyBusinessDba businessDba) |
| `BusinessAddressCountry` | [`CounterpartyBusinessAddressCountry`](../../doc/models/containers/counterparty-business-address-country.md) | Optional | This is a container for any-of cases. | CounterpartyBusinessAddressCountry getBusinessAddressCountry() | setBusinessAddressCountry(CounterpartyBusinessAddressCountry businessAddressCountry) |
| `BusinessStreetAddress1` | [`CounterpartyBusinessStreetAddress1`](../../doc/models/containers/counterparty-business-street-address-1.md) | Optional | This is a container for any-of cases. | CounterpartyBusinessStreetAddress1 getBusinessStreetAddress1() | setBusinessStreetAddress1(CounterpartyBusinessStreetAddress1 businessStreetAddress1) |
| `BusinessStreetAddress2` | [`CounterpartyBusinessStreetAddress2`](../../doc/models/containers/counterparty-business-street-address-2.md) | Optional | This is a container for any-of cases. | CounterpartyBusinessStreetAddress2 getBusinessStreetAddress2() | setBusinessStreetAddress2(CounterpartyBusinessStreetAddress2 businessStreetAddress2) |
| `BusinessCity` | [`CounterpartyBusinessCity`](../../doc/models/containers/counterparty-business-city.md) | Optional | This is a container for any-of cases. | CounterpartyBusinessCity getBusinessCity() | setBusinessCity(CounterpartyBusinessCity businessCity) |
| `BusinessState` | [`CounterpartyBusinessState`](../../doc/models/containers/counterparty-business-state.md) | Optional | This is a container for any-of cases. | CounterpartyBusinessState getBusinessState() | setBusinessState(CounterpartyBusinessState businessState) |
| `BusinessLegalEntityIdentifier` | [`CounterpartyBusinessLegalEntityIdentifier`](../../doc/models/containers/counterparty-business-legal-entity-identifier.md) | Optional | This is a container for any-of cases. | CounterpartyBusinessLegalEntityIdentifier getBusinessLegalEntityIdentifier() | setBusinessLegalEntityIdentifier(CounterpartyBusinessLegalEntityIdentifier businessLegalEntityIdentifier) |
| `CreatedAt` | `String` | Required | Creation timestamp in ISO 8601 format. | String getCreatedAt() | setCreatedAt(String createdAt) |
| `UpdatedAt` | `String` | Required | Last update timestamp in ISO 8601 format. | String getUpdatedAt() | setUpdatedAt(String updatedAt) |

## Example (as JSON)

```json
{
  "id": "id2",
  "workspace_id": "workspace_id4",
  "classification": "individual",
  "tenant_id": "String3",
  "individual_first_name": "String7",
  "individual_last_name": "String3",
  "individual_address_country": "String7",
  "individual_date_of_birth": "String9",
  "created_at": "created_at0",
  "updated_at": "updated_at2"
}
```

