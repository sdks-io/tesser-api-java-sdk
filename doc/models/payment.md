
# Payment

## Structure

`Payment`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Unique identifier for the payment. | String getId() | setId(String id) |
| `WorkspaceId` | `String` | Required | Workspace ID the payment belongs to. | String getWorkspaceId() | setWorkspaceId(String workspaceId) |
| `OrganizationReferenceId` | [`PaymentOrganizationReferenceId`](../../doc/models/containers/payment-organization-reference-id.md) | Optional | This is a container for any-of cases. | PaymentOrganizationReferenceId getOrganizationReferenceId() | setOrganizationReferenceId(PaymentOrganizationReferenceId organizationReferenceId) |
| `Direction` | [`DirectionEnum`](../../doc/models/direction-enum.md) | Required | Payment direction: 'inbound', 'outbound', 'internal'. | DirectionEnum getDirection() | setDirection(DirectionEnum direction) |
| `PaymentType` | [`PaymentTypeEnum`](../../doc/models/payment-type-enum.md) | Required | Type of payment operation: 'payment' (wallet-to-wallet), 'offramp' (crypto-to-fiat), 'onramp' (fiat-to-crypto), 'withdrawal', 'deposit', or 'transfer'. | PaymentTypeEnum getPaymentType() | setPaymentType(PaymentTypeEnum paymentType) |
| `SourceAccountId` | [`PaymentSourceAccountId`](../../doc/models/containers/payment-source-account-id.md) | Optional | This is a container for any-of cases. | PaymentSourceAccountId getSourceAccountId() | setSourceAccountId(PaymentSourceAccountId sourceAccountId) |
| `OriginatorAccountId` | [`PaymentOriginatorAccountId`](../../doc/models/containers/payment-originator-account-id.md) | Optional | This is a container for any-of cases. | PaymentOriginatorAccountId getOriginatorAccountId() | setOriginatorAccountId(PaymentOriginatorAccountId originatorAccountId) |
| `BeneficiaryAccountId` | [`PaymentBeneficiaryAccountId`](../../doc/models/containers/payment-beneficiary-account-id.md) | Optional | This is a container for any-of cases. | PaymentBeneficiaryAccountId getBeneficiaryAccountId() | setBeneficiaryAccountId(PaymentBeneficiaryAccountId beneficiaryAccountId) |
| `FromAmount` | `String` | Required | Amount to send. | String getFromAmount() | setFromAmount(String fromAmount) |
| `FromCurrency` | `String` | Required | Source currency code. | String getFromCurrency() | setFromCurrency(String fromCurrency) |
| `FromNetwork` | [`PaymentFromNetwork`](../../doc/models/containers/payment-from-network.md) | Optional | This is a container for any-of cases. | PaymentFromNetwork getFromNetwork() | setFromNetwork(PaymentFromNetwork fromNetwork) |
| `ToAmount` | `String` | Required | Amount to receive. | String getToAmount() | setToAmount(String toAmount) |
| `ToCurrency` | `String` | Required | Destination currency code. | String getToCurrency() | setToCurrency(String toCurrency) |
| `ToNetwork` | [`PaymentToNetwork`](../../doc/models/containers/payment-to-network.md) | Optional | This is a container for any-of cases. | PaymentToNetwork getToNetwork() | setToNetwork(PaymentToNetwork toNetwork) |
| `RiskStatus` | [`RiskStatusEnum`](../../doc/models/risk-status-enum.md) | Required | Current risk status. | RiskStatusEnum getRiskStatus() | setRiskStatus(RiskStatusEnum riskStatus) |
| `RiskStatusReasons` | `List<List<String>>` | Optional | List of reasons for risk status. | List<List<String>> getRiskStatusReasons() | setRiskStatusReasons(List<List<String>> riskStatusReasons) |
| `RiskReviewedBy` | [`PaymentRiskReviewedBy`](../../doc/models/containers/payment-risk-reviewed-by.md) | Optional | This is a container for any-of cases. | PaymentRiskReviewedBy getRiskReviewedBy() | setRiskReviewedBy(PaymentRiskReviewedBy riskReviewedBy) |
| `RiskReviewedAt` | [`PaymentRiskReviewedAt`](../../doc/models/containers/payment-risk-reviewed-at.md) | Optional | This is a container for any-of cases. | PaymentRiskReviewedAt getRiskReviewedAt() | setRiskReviewedAt(PaymentRiskReviewedAt riskReviewedAt) |
| `BalanceStatus` | [`PaymentBalanceStatus`](../../doc/models/containers/payment-balance-status.md) | Optional | This is a container for any-of cases. | PaymentBalanceStatus getBalanceStatus() | setBalanceStatus(PaymentBalanceStatus balanceStatus) |
| `BalanceReservedAt` | [`PaymentBalanceReservedAt`](../../doc/models/containers/payment-balance-reserved-at.md) | Optional | This is a container for any-of cases. | PaymentBalanceReservedAt getBalanceReservedAt() | setBalanceReservedAt(PaymentBalanceReservedAt balanceReservedAt) |
| `Steps` | [`List<Step>`](../../doc/models/step.md) | Optional | Optional list of system-generated steps that make up this payment/transfer route. | List<Step> getSteps() | setSteps(List<Step> steps) |
| `CreatedAt` | `LocalDateTime` | Required | ISO 8601 timestamp of creation. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `UpdatedAt` | `LocalDateTime` | Required | ISO 8601 timestamp of last update. | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |
| `ExpiresAt` | `LocalDateTime` | Required | ISO 8601 timestamp when the quote expires. | LocalDateTime getExpiresAt() | setExpiresAt(LocalDateTime expiresAt) |

## Example (as JSON)

```json
{
  "id": "id8",
  "workspace_id": "workspace_id0",
  "organization_reference_id": "String7",
  "direction": "outbound",
  "payment_type": "payment",
  "source_account_id": "String7",
  "originator_account_id": "String3",
  "beneficiary_account_id": "String7",
  "from_amount": "from_amount4",
  "from_currency": "from_currency0",
  "from_network": "String7",
  "to_amount": "to_amount0",
  "to_currency": "to_currency2",
  "risk_status": "unchecked",
  "created_at": "2016-03-13T12:52:32.123Z",
  "updated_at": "2016-03-13T12:52:32.123Z",
  "expires_at": "2016-03-13T12:52:32.123Z"
}
```

