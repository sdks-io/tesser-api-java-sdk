
# Transfer Step

## Structure

`TransferStep`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Unique identifier for the step. | String getId() | setId(String id) |
| `TransferId` | `String` | Required | ID of the parent payment/transfer. | String getTransferId() | setTransferId(String transferId) |
| `StepSequence` | `int` | Required | Step sequence number (0-based or 1-based).<br><br>**Constraints**: `>= -9007199254740991`, `<= 9007199254740991` | int getStepSequence() | setStepSequence(int stepSequence) |
| `StepType` | [`StepTypeEnum`](../../doc/models/step-type-enum.md) | Required | Step type: 'stablecoin_transfer', 'offramp', 'onramp', 'fiat_transfer'. | StepTypeEnum getStepType() | setStepType(StepTypeEnum stepType) |
| `FromAccountAssetId` | [`TransferStepFromAccountAssetId`](../../doc/models/containers/transfer-step-from-account-asset-id.md) | Optional | This is a container for any-of cases. | TransferStepFromAccountAssetId getFromAccountAssetId() | setFromAccountAssetId(TransferStepFromAccountAssetId fromAccountAssetId) |
| `FromAmount` | `String` | Required | Amount sent in this step. | String getFromAmount() | setFromAmount(String fromAmount) |
| `FromCurrency` | `String` | Required | Currency code sent in this step. | String getFromCurrency() | setFromCurrency(String fromCurrency) |
| `ToAccountAssetId` | [`TransferStepToAccountAssetId`](../../doc/models/containers/transfer-step-to-account-asset-id.md) | Optional | This is a container for any-of cases. | TransferStepToAccountAssetId getToAccountAssetId() | setToAccountAssetId(TransferStepToAccountAssetId toAccountAssetId) |
| `ToAmount` | `String` | Required | Amount received in this step. | String getToAmount() | setToAmount(String toAmount) |
| `ToCurrency` | `String` | Required | Currency code received in this step. | String getToCurrency() | setToCurrency(String toCurrency) |
| `TransactionHash` | [`TransferStepTransactionHash`](../../doc/models/containers/transfer-step-transaction-hash.md) | Optional | This is a container for any-of cases. | TransferStepTransactionHash getTransactionHash() | setTransactionHash(TransferStepTransactionHash transactionHash) |
| `Fees` | [`List<Fee1>`](../../doc/models/fee-1.md) | Optional | List of fees associated with this step. | List<Fee1> getFees() | setFees(List<Fee1> fees) |
| `ProviderKey` | [`TransferStepProviderKey`](../../doc/models/containers/transfer-step-provider-key.md) | Optional | This is a container for any-of cases. | TransferStepProviderKey getProviderKey() | setProviderKey(TransferStepProviderKey providerKey) |
| `Status` | [`StatusEnum`](../../doc/models/status-enum.md) | Required | Step status: 'created', 'submitted', 'confirmed', 'finalized', 'failed'. | StatusEnum getStatus() | setStatus(StatusEnum status) |
| `StatusReasons` | `List<List<String>>` | Optional | Array of reasons explaining the current status (if any). | List<List<String>> getStatusReasons() | setStatusReasons(List<List<String>> statusReasons) |
| `SubmittedAt` | [`TransferStepSubmittedAt`](../../doc/models/containers/transfer-step-submitted-at.md) | Optional | This is a container for any-of cases. | TransferStepSubmittedAt getSubmittedAt() | setSubmittedAt(TransferStepSubmittedAt submittedAt) |
| `ConfirmedAt` | [`TransferStepConfirmedAt`](../../doc/models/containers/transfer-step-confirmed-at.md) | Optional | This is a container for any-of cases. | TransferStepConfirmedAt getConfirmedAt() | setConfirmedAt(TransferStepConfirmedAt confirmedAt) |
| `FinalizedAt` | [`TransferStepFinalizedAt`](../../doc/models/containers/transfer-step-finalized-at.md) | Optional | This is a container for any-of cases. | TransferStepFinalizedAt getFinalizedAt() | setFinalizedAt(TransferStepFinalizedAt finalizedAt) |
| `CompletedAt` | [`TransferStepCompletedAt`](../../doc/models/containers/transfer-step-completed-at.md) | Optional | This is a container for any-of cases. | TransferStepCompletedAt getCompletedAt() | setCompletedAt(TransferStepCompletedAt completedAt) |
| `FailedAt` | [`TransferStepFailedAt`](../../doc/models/containers/transfer-step-failed-at.md) | Optional | This is a container for any-of cases. | TransferStepFailedAt getFailedAt() | setFailedAt(TransferStepFailedAt failedAt) |
| `CreatedAt` | `LocalDateTime` | Required | ISO 8601 timestamp of creation. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `UpdatedAt` | `LocalDateTime` | Required | ISO 8601 timestamp of last update. | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |
| `FromAccountId` | [`TransferStepFromAccountId`](../../doc/models/containers/transfer-step-from-account-id.md) | Optional | This is a container for any-of cases. | TransferStepFromAccountId getFromAccountId() | setFromAccountId(TransferStepFromAccountId fromAccountId) |
| `ToAccountId` | [`TransferStepToAccountId`](../../doc/models/containers/transfer-step-to-account-id.md) | Optional | This is a container for any-of cases. | TransferStepToAccountId getToAccountId() | setToAccountId(TransferStepToAccountId toAccountId) |

## Example (as JSON)

```json
{
  "id": "id4",
  "transfer_id": "transfer_id0",
  "step_sequence": 244,
  "step_type": "stablecoin_transfer",
  "from_account_asset_id": "String5",
  "from_amount": "from_amount0",
  "from_currency": "from_currency6",
  "to_account_asset_id": "String5",
  "to_amount": "to_amount6",
  "to_currency": "to_currency8",
  "transaction_hash": "String1",
  "fees": [
    {
      "fee_amount": "fee_amount2",
      "fee_currency": "fee_currency8",
      "type": "type0",
      "metadata": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "fee_amount": "fee_amount2",
      "fee_currency": "fee_currency8",
      "type": "type0",
      "metadata": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "provider_key": "alfred",
  "status": "submitted",
  "created_at": "2016-03-13T12:52:32.123Z",
  "updated_at": "2016-03-13T12:52:32.123Z"
}
```

