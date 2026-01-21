
# Create Counterparty Request

## Structure

`CreateCounterpartyRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Classification` | [`ClassificationEnum`](../../doc/models/classification-enum.md) | Required | Classification: 'individual' or 'business'. | ClassificationEnum getClassification() | setClassification(ClassificationEnum classification) |
| `TenantId` | [`CreateCounterpartyRequestTenantId`](../../doc/models/containers/create-counterparty-request-tenant-id.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestTenantId getTenantId() | setTenantId(CreateCounterpartyRequestTenantId tenantId) |
| `IndividualFirstName` | [`CreateCounterpartyRequestIndividualFirstName`](../../doc/models/containers/create-counterparty-request-individual-first-name.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestIndividualFirstName getIndividualFirstName() | setIndividualFirstName(CreateCounterpartyRequestIndividualFirstName individualFirstName) |
| `IndividualLastName` | [`CreateCounterpartyRequestIndividualLastName`](../../doc/models/containers/create-counterparty-request-individual-last-name.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestIndividualLastName getIndividualLastName() | setIndividualLastName(CreateCounterpartyRequestIndividualLastName individualLastName) |
| `IndividualAddressCountry` | [`CreateCounterpartyRequestIndividualAddressCountry`](../../doc/models/containers/create-counterparty-request-individual-address-country.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestIndividualAddressCountry getIndividualAddressCountry() | setIndividualAddressCountry(CreateCounterpartyRequestIndividualAddressCountry individualAddressCountry) |
| `IndividualDateOfBirth` | [`CreateCounterpartyRequestIndividualDateOfBirth`](../../doc/models/containers/create-counterparty-request-individual-date-of-birth.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestIndividualDateOfBirth getIndividualDateOfBirth() | setIndividualDateOfBirth(CreateCounterpartyRequestIndividualDateOfBirth individualDateOfBirth) |
| `IndividualNationalIdentificationNumber` | [`CreateCounterpartyRequestIndividualNationalIdentificationNumber`](../../doc/models/containers/create-counterparty-request-individual-national-identification-number.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestIndividualNationalIdentificationNumber getIndividualNationalIdentificationNumber() | setIndividualNationalIdentificationNumber(CreateCounterpartyRequestIndividualNationalIdentificationNumber individualNationalIdentificationNumber) |
| `IndividualStreetAddress1` | [`CreateCounterpartyRequestIndividualStreetAddress1`](../../doc/models/containers/create-counterparty-request-individual-street-address-1.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestIndividualStreetAddress1 getIndividualStreetAddress1() | setIndividualStreetAddress1(CreateCounterpartyRequestIndividualStreetAddress1 individualStreetAddress1) |
| `IndividualStreetAddress2` | [`CreateCounterpartyRequestIndividualStreetAddress2`](../../doc/models/containers/create-counterparty-request-individual-street-address-2.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestIndividualStreetAddress2 getIndividualStreetAddress2() | setIndividualStreetAddress2(CreateCounterpartyRequestIndividualStreetAddress2 individualStreetAddress2) |
| `IndividualCity` | [`CreateCounterpartyRequestIndividualCity`](../../doc/models/containers/create-counterparty-request-individual-city.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestIndividualCity getIndividualCity() | setIndividualCity(CreateCounterpartyRequestIndividualCity individualCity) |
| `IndividualState` | [`CreateCounterpartyRequestIndividualState`](../../doc/models/containers/create-counterparty-request-individual-state.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestIndividualState getIndividualState() | setIndividualState(CreateCounterpartyRequestIndividualState individualState) |
| `IndividualPostalCode` | [`CreateCounterpartyRequestIndividualPostalCode`](../../doc/models/containers/create-counterparty-request-individual-postal-code.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestIndividualPostalCode getIndividualPostalCode() | setIndividualPostalCode(CreateCounterpartyRequestIndividualPostalCode individualPostalCode) |
| `BusinessLegalName` | [`CreateCounterpartyRequestBusinessLegalName`](../../doc/models/containers/create-counterparty-request-business-legal-name.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestBusinessLegalName getBusinessLegalName() | setBusinessLegalName(CreateCounterpartyRequestBusinessLegalName businessLegalName) |
| `BusinessDba` | [`CreateCounterpartyRequestBusinessDba`](../../doc/models/containers/create-counterparty-request-business-dba.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestBusinessDba getBusinessDba() | setBusinessDba(CreateCounterpartyRequestBusinessDba businessDba) |
| `BusinessAddressCountry` | [`CreateCounterpartyRequestBusinessAddressCountry`](../../doc/models/containers/create-counterparty-request-business-address-country.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestBusinessAddressCountry getBusinessAddressCountry() | setBusinessAddressCountry(CreateCounterpartyRequestBusinessAddressCountry businessAddressCountry) |
| `BusinessStreetAddress1` | [`CreateCounterpartyRequestBusinessStreetAddress1`](../../doc/models/containers/create-counterparty-request-business-street-address-1.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestBusinessStreetAddress1 getBusinessStreetAddress1() | setBusinessStreetAddress1(CreateCounterpartyRequestBusinessStreetAddress1 businessStreetAddress1) |
| `BusinessStreetAddress2` | [`CreateCounterpartyRequestBusinessStreetAddress2`](../../doc/models/containers/create-counterparty-request-business-street-address-2.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestBusinessStreetAddress2 getBusinessStreetAddress2() | setBusinessStreetAddress2(CreateCounterpartyRequestBusinessStreetAddress2 businessStreetAddress2) |
| `BusinessCity` | [`CreateCounterpartyRequestBusinessCity`](../../doc/models/containers/create-counterparty-request-business-city.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestBusinessCity getBusinessCity() | setBusinessCity(CreateCounterpartyRequestBusinessCity businessCity) |
| `BusinessState` | [`CreateCounterpartyRequestBusinessState`](../../doc/models/containers/create-counterparty-request-business-state.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestBusinessState getBusinessState() | setBusinessState(CreateCounterpartyRequestBusinessState businessState) |
| `BusinessLegalEntityIdentifier` | [`CreateCounterpartyRequestBusinessLegalEntityIdentifier`](../../doc/models/containers/create-counterparty-request-business-legal-entity-identifier.md) | Optional | This is a container for any-of cases. | CreateCounterpartyRequestBusinessLegalEntityIdentifier getBusinessLegalEntityIdentifier() | setBusinessLegalEntityIdentifier(CreateCounterpartyRequestBusinessLegalEntityIdentifier businessLegalEntityIdentifier) |

## Example (as JSON)

```json
{
  "classification": "individual",
  "tenant_id": "0000073e-0000-0000-0000-000000000000",
  "individual_first_name": "String3",
  "individual_last_name": "String7",
  "individual_address_country": "String3",
  "individual_date_of_birth": "String7"
}
```

