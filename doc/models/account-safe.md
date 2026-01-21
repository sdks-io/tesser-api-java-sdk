
# Account Safe

## Structure

`AccountSafe`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Unique identifier for the account. | String getId() | setId(String id) |
| `WorkspaceId` | `String` | Optional | ID of the workspace. | String getWorkspaceId() | setWorkspaceId(String workspaceId) |
| `TenantId` | [`AccountSafeTenantId`](../../doc/models/containers/account-safe-tenant-id.md) | Optional | This is a container for any-of cases. | AccountSafeTenantId getTenantId() | setTenantId(AccountSafeTenantId tenantId) |
| `CounterpartyId` | [`AccountSafeCounterpartyId`](../../doc/models/containers/account-safe-counterparty-id.md) | Optional | This is a container for any-of cases. | AccountSafeCounterpartyId getCounterpartyId() | setCounterpartyId(AccountSafeCounterpartyId counterpartyId) |
| `Type` | [`TypeEnum`](../../doc/models/type-enum.md) | Required | Account type. | TypeEnum getType() | setType(TypeEnum type) |
| `Name` | `String` | Required | Account name. | String getName() | setName(String name) |
| `BankName` | [`AccountSafeBankName`](../../doc/models/containers/account-safe-bank-name.md) | Optional | This is a container for any-of cases. | AccountSafeBankName getBankName() | setBankName(AccountSafeBankName bankName) |
| `BankCodeType` | [`AccountSafeBankCodeType`](../../doc/models/containers/account-safe-bank-code-type.md) | Optional | This is a container for any-of cases. | AccountSafeBankCodeType getBankCodeType() | setBankCodeType(AccountSafeBankCodeType bankCodeType) |
| `BankIdentifierCode` | [`AccountSafeBankIdentifierCode`](../../doc/models/containers/account-safe-bank-identifier-code.md) | Optional | This is a container for any-of cases. | AccountSafeBankIdentifierCode getBankIdentifierCode() | setBankIdentifierCode(AccountSafeBankIdentifierCode bankIdentifierCode) |
| `CryptoWalletAddress` | [`AccountSafeCryptoWalletAddress`](../../doc/models/containers/account-safe-crypto-wallet-address.md) | Optional | This is a container for any-of cases. | AccountSafeCryptoWalletAddress getCryptoWalletAddress() | setCryptoWalletAddress(AccountSafeCryptoWalletAddress cryptoWalletAddress) |
| `CreatedAt` | `String` | Required | Creation timestamp. | String getCreatedAt() | setCreatedAt(String createdAt) |
| `UpdatedAt` | `String` | Required | Last update timestamp. | String getUpdatedAt() | setUpdatedAt(String updatedAt) |

## Example (as JSON)

```json
{
  "id": "id2",
  "workspace_id": "b53f6690-3242-4942-9907-885779632832",
  "type": "fiat_bank",
  "name": "name2",
  "created_at": "created_at0",
  "updated_at": "updated_at2",
  "tenant_id": "String3",
  "counterparty_id": "String3",
  "bank_name": "String3",
  "bank_code_type": "String9"
}
```

