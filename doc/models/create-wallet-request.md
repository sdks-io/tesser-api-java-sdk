
# Create Wallet Request

## Structure

`CreateWalletRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `WorkspaceId` | `String` | Required | ID of the workspace. | String getWorkspaceId() | setWorkspaceId(String workspaceId) |
| `TenantId` | `String` | Optional | ID of the tenant that owns this wallet (optional). At most one of tenant_id or counterparty_id may be provided. | String getTenantId() | setTenantId(String tenantId) |
| `CounterpartyId` | `String` | Optional | ID of the counterparty that owns this wallet (optional). At most one of tenant_id or counterparty_id may be provided. | String getCounterpartyId() | setCounterpartyId(String counterpartyId) |
| `Name` | `String` | Required | Name of the wallet account.<br><br>**Constraints**: *Minimum Length*: `1` | String getName() | setName(String name) |
| `Type` | [`Type3Enum`](../../doc/models/type-3-enum.md) | Required | Wallet type. | Type3Enum getType() | setType(Type3Enum type) |
| `Signature` | `String` | Required | A cryptographic stamp used to verify the integrity and authenticity of the request. This ensures the request was signed by an authorized key. See Documentation > Signing for more details. | String getSignature() | setSignature(String signature) |

## Example (as JSON)

```json
{
  "workspace_id": "b53f6690-3242-4942-9907-885779632832",
  "tenant_id": "44031e7e-d416-45f0-a46b-ded12b9751ca",
  "counterparty_id": "96339002-c92e-4422-995f-39599528659b",
  "name": "Treasury Wallet EU",
  "type": "stablecoin_stellar",
  "signature": "eyJwdWJsaWNLZXkiOiJwdWJfZXhhbXBsZSIsInNpZ25hdHVyZSI6InNpZ19leGFtcGxlIiwic2NoZW1lIjoiRUQyNTUxOSJ9"
}
```

