
# Fee 1

## Structure

`Fee1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FeeAmount` | `String` | Required | Fee amount. | String getFeeAmount() | setFeeAmount(String feeAmount) |
| `FeeCurrency` | `String` | Required | Fee currency code. | String getFeeCurrency() | setFeeCurrency(String feeCurrency) |
| `Type` | `String` | Required | Fee type (e.g., 'gas', 'provider'). | String getType() | setType(String type) |
| `Metadata` | [`Fee1Metadata`](../../doc/models/containers/fee-1-metadata.md) | Optional | This is a container for any-of cases. | Fee1Metadata getMetadata() | setMetadata(Fee1Metadata metadata) |

## Example (as JSON)

```json
{
  "fee_amount": "fee_amount6",
  "fee_currency": "fee_currency6",
  "type": "type8",
  "metadata": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

