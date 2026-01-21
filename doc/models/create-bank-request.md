
# Create Bank Request

## Structure

`CreateBankRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `WorkspaceId` | `String` | Optional | ID of the workspace. | String getWorkspaceId() | setWorkspaceId(String workspaceId) |
| `Name` | `String` | Required | Name of the bank account.<br><br>**Constraints**: *Minimum Length*: `1` | String getName() | setName(String name) |
| `BankName` | `String` | Required | Name of the bank.<br><br>**Constraints**: *Minimum Length*: `1` | String getBankName() | setBankName(String bankName) |
| `BankCodeType` | `String` | Required | Type of bank code (e.g., 'SWIFT').<br><br>**Constraints**: *Minimum Length*: `1` | String getBankCodeType() | setBankCodeType(String bankCodeType) |
| `BankIdentifierCode` | `String` | Required | Bank identifier code value.<br><br>**Constraints**: *Minimum Length*: `1` | String getBankIdentifierCode() | setBankIdentifierCode(String bankIdentifierCode) |
| `BankAccountNumber` | `String` | Required | Bank account number (IBAN, etc).<br><br>**Constraints**: *Minimum Length*: `1` | String getBankAccountNumber() | setBankAccountNumber(String bankAccountNumber) |
| `CounterpartyId` | `String` | Optional | ID of the counterparty owner. | String getCounterpartyId() | setCounterpartyId(String counterpartyId) |

## Example (as JSON)

```json
{
  "workspace_id": "b53f6690-3242-4942-9907-885779632832",
  "name": "Operating Account - EU",
  "bank_name": "Chase Bank",
  "bank_code_type": "SWIFT",
  "bank_identifier_code": "CHASUS33",
  "bank_account_number": "123456789",
  "counterparty_id": "counterparty_id2"
}
```

