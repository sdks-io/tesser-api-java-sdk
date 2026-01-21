
# Create Deposit Request

## Structure

`CreateDepositRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FromCurrency` | `String` | Required | Source currency code. | String getFromCurrency() | setFromCurrency(String fromCurrency) |
| `ToCurrency` | `String` | Required | Destination currency code. | String getToCurrency() | setToCurrency(String toCurrency) |
| `FromAmount` | `String` | Optional | Amount to send. Required if to_amount is missing. | String getFromAmount() | setFromAmount(String fromAmount) |
| `ToAmount` | `String` | Optional | Amount to receive. Required if from_amount is missing. | String getToAmount() | setToAmount(String toAmount) |
| `TenantId` | `String` | Optional | Optional tenant ID. | String getTenantId() | setTenantId(String tenantId) |
| `ToAccountId` | `String` | Required | Destination account ID. | String getToAccountId() | setToAccountId(String toAccountId) |
| `ToNetwork` | `String` | Required | Network for the deposit. | String getToNetwork() | setToNetwork(String toNetwork) |

## Example (as JSON)

```json
{
  "from_currency": "from_currency4",
  "to_currency": "to_currency6",
  "from_amount": "from_amount8",
  "to_amount": "to_amount4",
  "tenant_id": "tenant_id2",
  "to_account_id": "to_account_id0",
  "to_network": "to_network4"
}
```

