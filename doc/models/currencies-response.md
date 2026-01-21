
# Currencies Response

## Structure

`CurrenciesResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`List<Currency>`](../../doc/models/currency.md) | Required | List of all supported currencies | List<Currency> getData() | setData(List<Currency> data) |

## Example (as JSON)

```json
{
  "data": [
    {
      "name": "name0",
      "key": "key0",
      "decimals": 174.24,
      "network": "String7"
    }
  ]
}
```

