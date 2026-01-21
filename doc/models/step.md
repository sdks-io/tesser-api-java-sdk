
# Step

## Structure

`Step`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Unique identifier for the step. | String getId() | setId(String id) |
| `TransferId` | `String` | Required | ID of the parent payment/transfer. | String getTransferId() | setTransferId(String transferId) |
| `StepSequence` | `int` | Required | Step sequence number (0-based or 1-based).<br><br>**Constraints**: `>= -9007199254740991`, `<= 9007199254740991` | int getStepSequence() | setStepSequence(int stepSequence) |
| `StepType` | [`StepTypeEnum`](../../doc/models/step-type-enum.md) | Required | Step type: 'stablecoin_transfer', 'offramp', 'onramp', 'fiat_transfer'. | StepTypeEnum getStepType() | setStepType(StepTypeEnum stepType) |
| `FromAccountAssetId` | [`StepFromAccountAssetId`](../../doc/models/containers/step-from-account-asset-id.md) | Optional | This is a container for any-of cases. | StepFromAccountAssetId getFromAccountAssetId() | setFromAccountAssetId(StepFromAccountAssetId fromAccountAssetId) |
| `FromAccountId` | [`StepFromAccountId`](../../doc/models/containers/step-from-account-id.md) | Optional | This is a container for any-of cases. | StepFromAccountId getFromAccountId() | setFromAccountId(StepFromAccountId fromAccountId) |
| `FromAmount` | `String` | Required | Amount sent in this step. | String getFromAmount() | setFromAmount(String fromAmount) |
| `FromCurrency` | `String` | Required | Currency code sent in this step. | String getFromCurrency() | setFromCurrency(String fromCurrency) |
| `ToAccountAssetId` | [`StepToAccountAssetId`](../../doc/models/containers/step-to-account-asset-id.md) | Optional | This is a container for any-of cases. | StepToAccountAssetId getToAccountAssetId() | setToAccountAssetId(StepToAccountAssetId toAccountAssetId) |
| `ToAccountId` | [`StepToAccountId`](../../doc/models/containers/step-to-account-id.md) | Optional | This is a container for any-of cases. | StepToAccountId getToAccountId() | setToAccountId(StepToAccountId toAccountId) |
| `ToAmount` | `String` | Required | Amount received in this step. | String getToAmount() | setToAmount(String toAmount) |
| `ToCurrency` | `String` | Required | Currency code received in this step. | String getToCurrency() | setToCurrency(String toCurrency) |
| `TransactionHash` | [`StepTransactionHash`](../../doc/models/containers/step-transaction-hash.md) | Optional | This is a container for any-of cases. | StepTransactionHash getTransactionHash() | setTransactionHash(StepTransactionHash transactionHash) |
| `Fees` | [`List<Fee1>`](../../doc/models/fee-1.md) | Optional | List of fees associated with this step. | List<Fee1> getFees() | setFees(List<Fee1> fees) |
| `ProviderKey` | [`StepProviderKey`](../../doc/models/containers/step-provider-key.md) | Optional | This is a container for any-of cases. | StepProviderKey getProviderKey() | setProviderKey(StepProviderKey providerKey) |
| `Status` | [`Status1Enum`](../../doc/models/status-1-enum.md) | Required | Step status: 'created', 'submitted', 'confirmed', 'finalized', 'failed'. | Status1Enum getStatus() | setStatus(Status1Enum status) |
| `StatusReasons` | [`StepStatusReasons`](../../doc/models/containers/step-status-reasons.md) | Optional | This is a container for any-of cases. | StepStatusReasons getStatusReasons() | setStatusReasons(StepStatusReasons statusReasons) |
| `SubmittedAt` | [`StepSubmittedAt`](../../doc/models/containers/step-submitted-at.md) | Optional | This is a container for any-of cases. | StepSubmittedAt getSubmittedAt() | setSubmittedAt(StepSubmittedAt submittedAt) |
| `ConfirmedAt` | [`StepConfirmedAt`](../../doc/models/containers/step-confirmed-at.md) | Optional | This is a container for any-of cases. | StepConfirmedAt getConfirmedAt() | setConfirmedAt(StepConfirmedAt confirmedAt) |
| `FinalizedAt` | [`StepFinalizedAt`](../../doc/models/containers/step-finalized-at.md) | Optional | This is a container for any-of cases. | StepFinalizedAt getFinalizedAt() | setFinalizedAt(StepFinalizedAt finalizedAt) |
| `CompletedAt` | [`StepCompletedAt`](../../doc/models/containers/step-completed-at.md) | Optional | This is a container for any-of cases. | StepCompletedAt getCompletedAt() | setCompletedAt(StepCompletedAt completedAt) |
| `FailedAt` | [`StepFailedAt`](../../doc/models/containers/step-failed-at.md) | Optional | This is a container for any-of cases. | StepFailedAt getFailedAt() | setFailedAt(StepFailedAt failedAt) |
| `CreatedAt` | `LocalDateTime` | Required | ISO 8601 timestamp of creation. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `UpdatedAt` | `LocalDateTime` | Required | ISO 8601 timestamp of last update. | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |

## Example (as JSON)

```json
{
  "id": "id0",
  "transfer_id": "transfer_id6",
  "step_sequence": 202,
  "step_type": "onramp",
  "from_account_asset_id": "String1",
  "from_account_id": "String7",
  "from_amount": "from_amount6",
  "from_currency": "from_currency2",
  "to_account_asset_id": "String1",
  "to_account_id": "String9",
  "to_amount": "to_amount2",
  "to_currency": "to_currency4",
  "transaction_hash": "String5",
  "status": "completed",
  "created_at": "2016-03-13T12:52:32.123Z",
  "updated_at": "2016-03-13T12:52:32.123Z"
}
```

