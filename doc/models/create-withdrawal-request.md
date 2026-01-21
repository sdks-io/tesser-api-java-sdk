
# Create Withdrawal Request

## Structure

`CreateWithdrawalRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ToAccountId` | `String` | Required | Destination account ID. | String getToAccountId() | setToAccountId(String toAccountId) |
| `FromCurrency` | `String` | Required | Source currency code. | String getFromCurrency() | setFromCurrency(String fromCurrency) |
| `ToCurrency` | `String` | Required | Destination currency code. | String getToCurrency() | setToCurrency(String toCurrency) |
| `FromAmount` | `String` | Optional | Amount to send. Required if to_amount is missing. | String getFromAmount() | setFromAmount(String fromAmount) |
| `ToAmount` | `String` | Optional | Amount to receive. Required if from_amount is missing. | String getToAmount() | setToAmount(String toAmount) |
| `TenantId` | `String` | Optional | Optional tenant ID. | String getTenantId() | setTenantId(String tenantId) |
| `FromAccountId` | `String` | Required | Source account ID. | String getFromAccountId() | setFromAccountId(String fromAccountId) |
| `FromNetwork` | `String` | Required | Network for the withdrawal. | String getFromNetwork() | setFromNetwork(String fromNetwork) |

## Example (as JSON)

```json
{
  "to_account_id": "to_account_id4",
  "from_currency": "from_currency8",
  "to_currency": "to_currency0",
  "from_amount": "from_amount2",
  "to_amount": "to_amount8",
  "tenant_id": "tenant_id6",
  "from_account_id": "from_account_id2",
  "from_network": "from_network4"
}
```

