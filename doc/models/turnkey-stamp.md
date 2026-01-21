
# Turnkey Stamp

Optional Turnkey stamp data for server-side signing

## Structure

`TurnkeyStamp`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StampHeaderName` | `String` | Required | - | String getStampHeaderName() | setStampHeaderName(String stampHeaderName) |
| `StampHeaderValue` | `String` | Required | - | String getStampHeaderValue() | setStampHeaderValue(String stampHeaderValue) |
| `TurnkeyBody` | `String` | Required | - | String getTurnkeyBody() | setTurnkeyBody(String turnkeyBody) |

## Example (as JSON)

```json
{
  "stampHeaderName": "stampHeaderName8",
  "stampHeaderValue": "stampHeaderValue2",
  "turnkeyBody": "turnkeyBody4"
}
```

