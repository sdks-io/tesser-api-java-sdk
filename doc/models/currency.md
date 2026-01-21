
# Currency

## Structure

`Currency`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | Display name for the currency (e.g., 'Circle USD') | String getName() | setName(String name) |
| `Key` | `String` | Required | Currency code/key (e.g., 'USDC', 'USD') | String getKey() | setKey(String key) |
| `Decimals` | `double` | Required | Number of decimal places for the currency | double getDecimals() | setDecimals(double decimals) |
| `Network` | [`CurrencyNetwork`](../../doc/models/containers/currency-network.md) | Required | This is a container for any-of cases. | CurrencyNetwork getNetwork() | setNetwork(CurrencyNetwork network) |

## Example (as JSON)

```json
{
  "name": "name8",
  "key": "key8",
  "decimals": 116.22,
  "network": "String5"
}
```

