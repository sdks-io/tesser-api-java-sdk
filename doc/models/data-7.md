
# Data 7

## Structure

`Data7`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Unique identifier for the payment | String getId() | setId(String id) |
| `WorkspaceId` | `String` | Required | Workspace ID the payment belongs to | String getWorkspaceId() | setWorkspaceId(String workspaceId) |
| `OrganizationReferenceId` | [`Data7OrganizationReferenceId`](../../doc/models/containers/data-7-organization-reference-id.md) | Optional | This is a container for any-of cases. | Data7OrganizationReferenceId getOrganizationReferenceId() | setOrganizationReferenceId(Data7OrganizationReferenceId organizationReferenceId) |
| `Direction` | [`Direction1Enum`](../../doc/models/direction-1-enum.md) | Required | Payment direction: 'inbound', 'outbound', 'internal' | Direction1Enum getDirection() | setDirection(Direction1Enum direction) |
| `PaymentType` | [`PaymentTypeEnum`](../../doc/models/payment-type-enum.md) | Required | Type of payment operation: 'payment' (wallet-to-wallet), 'offramp' (crypto-to-fiat), 'onramp' (fiat-to-crypto), 'withdrawal', 'deposit', or 'transfer'. | PaymentTypeEnum getPaymentType() | setPaymentType(PaymentTypeEnum paymentType) |
| `SourceAccountId` | [`Data7SourceAccountId`](../../doc/models/containers/data-7-source-account-id.md) | Optional | This is a container for any-of cases. | Data7SourceAccountId getSourceAccountId() | setSourceAccountId(Data7SourceAccountId sourceAccountId) |
| `OriginatorAccountId` | [`Data7OriginatorAccountId`](../../doc/models/containers/data-7-originator-account-id.md) | Optional | This is a container for any-of cases. | Data7OriginatorAccountId getOriginatorAccountId() | setOriginatorAccountId(Data7OriginatorAccountId originatorAccountId) |
| `BeneficiaryAccountId` | [`Data7BeneficiaryAccountId`](../../doc/models/containers/data-7-beneficiary-account-id.md) | Optional | This is a container for any-of cases. | Data7BeneficiaryAccountId getBeneficiaryAccountId() | setBeneficiaryAccountId(Data7BeneficiaryAccountId beneficiaryAccountId) |
| `FromAmount` | `String` | Required | Amount to send. | String getFromAmount() | setFromAmount(String fromAmount) |
| `FromCurrency` | `String` | Required | Source currency code. | String getFromCurrency() | setFromCurrency(String fromCurrency) |
| `FromNetwork` | [`Data7FromNetwork`](../../doc/models/containers/data-7-from-network.md) | Optional | This is a container for any-of cases. | Data7FromNetwork getFromNetwork() | setFromNetwork(Data7FromNetwork fromNetwork) |
| `ToAmount` | `String` | Required | Amount to receive. | String getToAmount() | setToAmount(String toAmount) |
| `ToCurrency` | `String` | Required | Destination currency code. | String getToCurrency() | setToCurrency(String toCurrency) |
| `ToNetwork` | [`Data7ToNetwork`](../../doc/models/containers/data-7-to-network.md) | Optional | This is a container for any-of cases. | Data7ToNetwork getToNetwork() | setToNetwork(Data7ToNetwork toNetwork) |
| `RiskStatus` | [`RiskStatusEnum`](../../doc/models/risk-status-enum.md) | Required | Current risk status. | RiskStatusEnum getRiskStatus() | setRiskStatus(RiskStatusEnum riskStatus) |
| `RiskStatusReasons` | [`Data7RiskStatusReasons`](../../doc/models/containers/data-7-risk-status-reasons.md) | Optional | This is a container for any-of cases. | Data7RiskStatusReasons getRiskStatusReasons() | setRiskStatusReasons(Data7RiskStatusReasons riskStatusReasons) |
| `RiskReviewedBy` | [`Data7RiskReviewedBy`](../../doc/models/containers/data-7-risk-reviewed-by.md) | Optional | This is a container for any-of cases. | Data7RiskReviewedBy getRiskReviewedBy() | setRiskReviewedBy(Data7RiskReviewedBy riskReviewedBy) |
| `RiskReviewedAt` | [`Data7RiskReviewedAt`](../../doc/models/containers/data-7-risk-reviewed-at.md) | Optional | This is a container for any-of cases. | Data7RiskReviewedAt getRiskReviewedAt() | setRiskReviewedAt(Data7RiskReviewedAt riskReviewedAt) |
| `BalanceStatus` | [`Data7BalanceStatus`](../../doc/models/containers/data-7-balance-status.md) | Optional | This is a container for any-of cases. | Data7BalanceStatus getBalanceStatus() | setBalanceStatus(Data7BalanceStatus balanceStatus) |
| `BalanceReservedAt` | [`Data7BalanceReservedAt`](../../doc/models/containers/data-7-balance-reserved-at.md) | Optional | This is a container for any-of cases. | Data7BalanceReservedAt getBalanceReservedAt() | setBalanceReservedAt(Data7BalanceReservedAt balanceReservedAt) |
| `Steps` | [`List<Step>`](../../doc/models/step.md) | Optional | Optional list of system-generated steps that make up this payment/transfer route. | List<Step> getSteps() | setSteps(List<Step> steps) |
| `CreatedAt` | `LocalDateTime` | Required | ISO 8601 timestamp of creation. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `UpdatedAt` | `LocalDateTime` | Required | ISO 8601 timestamp of last update. | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |
| `ExpiresAt` | `LocalDateTime` | Required | ISO 8601 timestamp when the quote expires. | LocalDateTime getExpiresAt() | setExpiresAt(LocalDateTime expiresAt) |

## Example (as JSON)

```json
{
  "id": "id4",
  "workspace_id": "workspace_id6",
  "organization_reference_id": "String3",
  "direction": "inbound",
  "payment_type": "onramp",
  "source_account_id": "String3",
  "originator_account_id": "String7",
  "beneficiary_account_id": "String1",
  "from_amount": "from_amount0",
  "from_currency": "from_currency6",
  "from_network": "String3",
  "to_amount": "to_amount6",
  "to_currency": "to_currency8",
  "risk_status": "approved",
  "created_at": "2016-03-13T12:52:32.123Z",
  "updated_at": "2016-03-13T12:52:32.123Z",
  "expires_at": "2016-03-13T12:52:32.123Z"
}
```

