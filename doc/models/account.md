
# Account

## Structure

`Account`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Unique identifier for the account. | String getId() | setId(String id) |
| `WorkspaceId` | `String` | Optional | ID of the workspace. | String getWorkspaceId() | setWorkspaceId(String workspaceId) |
| `TenantId` | [`AccountTenantId`](../../doc/models/containers/account-tenant-id.md) | Optional | This is a container for any-of cases. | AccountTenantId getTenantId() | setTenantId(AccountTenantId tenantId) |
| `CounterpartyId` | [`AccountCounterpartyId`](../../doc/models/containers/account-counterparty-id.md) | Optional | This is a container for any-of cases. | AccountCounterpartyId getCounterpartyId() | setCounterpartyId(AccountCounterpartyId counterpartyId) |
| `Type` | [`TypeEnum`](../../doc/models/type-enum.md) | Required | Account type. | TypeEnum getType() | setType(TypeEnum type) |
| `Name` | `String` | Required | Account name. | String getName() | setName(String name) |
| `BankName` | [`AccountBankName`](../../doc/models/containers/account-bank-name.md) | Optional | This is a container for any-of cases. | AccountBankName getBankName() | setBankName(AccountBankName bankName) |
| `BankCodeType` | [`AccountBankCodeType`](../../doc/models/containers/account-bank-code-type.md) | Optional | This is a container for any-of cases. | AccountBankCodeType getBankCodeType() | setBankCodeType(AccountBankCodeType bankCodeType) |
| `BankIdentifierCode` | [`AccountBankIdentifierCode`](../../doc/models/containers/account-bank-identifier-code.md) | Optional | This is a container for any-of cases. | AccountBankIdentifierCode getBankIdentifierCode() | setBankIdentifierCode(AccountBankIdentifierCode bankIdentifierCode) |
| `CryptoWalletAddress` | [`AccountCryptoWalletAddress`](../../doc/models/containers/account-crypto-wallet-address.md) | Optional | This is a container for any-of cases. | AccountCryptoWalletAddress getCryptoWalletAddress() | setCryptoWalletAddress(AccountCryptoWalletAddress cryptoWalletAddress) |
| `BankAccountNumber` | [`AccountBankAccountNumber`](../../doc/models/containers/account-bank-account-number.md) | Optional | This is a container for any-of cases. | AccountBankAccountNumber getBankAccountNumber() | setBankAccountNumber(AccountBankAccountNumber bankAccountNumber) |
| `CreatedAt` | `String` | Required | Creation timestamp. | String getCreatedAt() | setCreatedAt(String createdAt) |
| `UpdatedAt` | `String` | Required | Last update timestamp. | String getUpdatedAt() | setUpdatedAt(String updatedAt) |

## Example (as JSON)

```json
{
  "id": "id8",
  "workspace_id": "b53f6690-3242-4942-9907-885779632832",
  "type": "stablecoin_solana",
  "name": "name8",
  "created_at": "created_at6",
  "updated_at": "updated_at4",
  "tenant_id": "String9",
  "counterparty_id": "String7",
  "bank_name": "String7",
  "bank_code_type": "String5"
}
```

