
# Update Payment Request

## Structure

`UpdatePaymentRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `OriginatorAccountId` | `String` | Required | ID of the account originating the payment. | String getOriginatorAccountId() | setOriginatorAccountId(String originatorAccountId) |
| `SourceAccountId` | `String` | Required | ID of the source account (e.g., wallet). | String getSourceAccountId() | setSourceAccountId(String sourceAccountId) |
| `BeneficiaryAccountId` | `String` | Required | ID of the beneficiary account. | String getBeneficiaryAccountId() | setBeneficiaryAccountId(String beneficiaryAccountId) |
| `OrganizationReferenceId` | `String` | Optional | Optional external reference ID to update. | String getOrganizationReferenceId() | setOrganizationReferenceId(String organizationReferenceId) |

## Example (as JSON)

```json
{
  "originator_account_id": "originator_account_id2",
  "source_account_id": "source_account_id6",
  "beneficiary_account_id": "beneficiary_account_id6",
  "organization_reference_id": "organization_reference_id6"
}
```

