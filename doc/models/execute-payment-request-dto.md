
# Execute Payment Request Dto

## Structure

`ExecutePaymentRequestDto`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Signature` | `String` | Required | Signature for the specified payment step. | String getSignature() | setSignature(String signature) |
| `TurnkeyStamp` | [`TurnkeyStamp`](../../doc/models/turnkey-stamp.md) | Optional | Optional Turnkey stamp data for server-side signing | TurnkeyStamp getTurnkeyStamp() | setTurnkeyStamp(TurnkeyStamp turnkeyStamp) |

## Example (as JSON)

```json
{
  "signature": "signature6",
  "turnkey_stamp": {
    "stampHeaderName": "stampHeaderName0",
    "stampHeaderValue": "stampHeaderValue4",
    "turnkeyBody": "turnkeyBody2"
  }
}
```

