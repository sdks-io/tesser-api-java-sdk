
# Create Payment Request

## Structure

`CreatePaymentRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FromCurrency` | `String` | Required | Source currency code (e.g., 'USDC'). See GET /currencies for supported values.<br><br>**Constraints**: *Minimum Length*: `1` | String getFromCurrency() | setFromCurrency(String fromCurrency) |
| `ToCurrency` | `String` | Required | Destination currency code (e.g., 'USD'). See GET /currencies for supported values.<br><br>**Constraints**: *Minimum Length*: `1` | String getToCurrency() | setToCurrency(String toCurrency) |
| `FromAmount` | `String` | Optional | Amount to send in source currency units. Required if to_amount is not provided. | String getFromAmount() | setFromAmount(String fromAmount) |
| `ToAmount` | `String` | Optional | Amount to receive in destination currency units. Required if from_amount is not provided. | String getToAmount() | setToAmount(String toAmount) |
| `FromNetwork` | `String` | Optional | Blockchain network for source currency (e.g., 'POLYGON'). See GET /networks for supported values.<br><br>**Constraints**: *Minimum Length*: `1` | String getFromNetwork() | setFromNetwork(String fromNetwork) |
| `ToNetwork` | `String` | Optional | Blockchain network for destination currency (if applicable). See GET /networks for supported values.<br><br>**Constraints**: *Minimum Length*: `1` | String getToNetwork() | setToNetwork(String toNetwork) |
| `OrganizationReferenceId` | `String` | Optional | Optional external reference ID for the organization. | String getOrganizationReferenceId() | setOrganizationReferenceId(String organizationReferenceId) |
| `OriginatorAccountId` | `String` | Optional | ID of the account originating the payment. | String getOriginatorAccountId() | setOriginatorAccountId(String originatorAccountId) |
| `SourceAccountId` | `String` | Optional | ID of the source account (e.g., wallet). | String getSourceAccountId() | setSourceAccountId(String sourceAccountId) |
| `BeneficiaryAccountId` | `String` | Optional | ID of the beneficiary account. | String getBeneficiaryAccountId() | setBeneficiaryAccountId(String beneficiaryAccountId) |

## Example (as JSON)

```json
{
  "from_currency": "from_currency8",
  "to_currency": "to_currency0",
  "from_amount": "from_amount2",
  "to_amount": "to_amount8",
  "from_network": "from_network4",
  "to_network": "to_network8",
  "organization_reference_id": "organization_reference_id4"
}
```

