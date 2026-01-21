
# Account List Item

## Structure

`AccountListItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Unique identifier for the account. | String getId() | setId(String id) |
| `WorkspaceId` | `String` | Optional | ID of the workspace. | String getWorkspaceId() | setWorkspaceId(String workspaceId) |
| `TenantId` | [`AccountListItemTenantId`](../../doc/models/containers/account-list-item-tenant-id.md) | Optional | This is a container for any-of cases. | AccountListItemTenantId getTenantId() | setTenantId(AccountListItemTenantId tenantId) |
| `CounterpartyId` | [`AccountListItemCounterpartyId`](../../doc/models/containers/account-list-item-counterparty-id.md) | Optional | This is a container for any-of cases. | AccountListItemCounterpartyId getCounterpartyId() | setCounterpartyId(AccountListItemCounterpartyId counterpartyId) |
| `Type` | [`TypeEnum`](../../doc/models/type-enum.md) | Required | Account type. | TypeEnum getType() | setType(TypeEnum type) |
| `Name` | `String` | Required | Account name. | String getName() | setName(String name) |
| `BankName` | [`AccountListItemBankName`](../../doc/models/containers/account-list-item-bank-name.md) | Optional | This is a container for any-of cases. | AccountListItemBankName getBankName() | setBankName(AccountListItemBankName bankName) |
| `BankCodeType` | [`AccountListItemBankCodeType`](../../doc/models/containers/account-list-item-bank-code-type.md) | Optional | This is a container for any-of cases. | AccountListItemBankCodeType getBankCodeType() | setBankCodeType(AccountListItemBankCodeType bankCodeType) |
| `BankIdentifierCode` | [`AccountListItemBankIdentifierCode`](../../doc/models/containers/account-list-item-bank-identifier-code.md) | Optional | This is a container for any-of cases. | AccountListItemBankIdentifierCode getBankIdentifierCode() | setBankIdentifierCode(AccountListItemBankIdentifierCode bankIdentifierCode) |
| `CryptoWalletAddress` | [`AccountListItemCryptoWalletAddress`](../../doc/models/containers/account-list-item-crypto-wallet-address.md) | Optional | This is a container for any-of cases. | AccountListItemCryptoWalletAddress getCryptoWalletAddress() | setCryptoWalletAddress(AccountListItemCryptoWalletAddress cryptoWalletAddress) |
| `BankAccountNumber` | [`AccountListItemBankAccountNumber`](../../doc/models/containers/account-list-item-bank-account-number.md) | Optional | This is a container for any-of cases. | AccountListItemBankAccountNumber getBankAccountNumber() | setBankAccountNumber(AccountListItemBankAccountNumber bankAccountNumber) |
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
  "counterparty_id": "String5",
  "bank_name": "String5",
  "bank_code_type": "String5"
}
```

