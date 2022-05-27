> class `TransactionRecord`

Response when the client sends the node TransactionGetRecordResponse

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): `TransactionRecord`

Decode a `TransactionRecord` from an appropriate protobuf encode structure

---

### Methods

##### `toBytes` (): `bytes`

The byte representation of the encoded protobuf type

---

##### `toString` (): `String`

Stringification of all the current values

---

### Fields

### `receipt`: [`TransactionReceipt`](reference/core/TransactionReceipt.md)

Receipt for the transaction

---

### `transactionHash`: `bytes`

Hash of the transaction

---

### `consensusTimestamp`: `Timestamp`

The timestamp the transaction came to consensus

---

### `transactionId`: [`TransactionId`](reference/core/TransactionId.md)

Transaction ID of the transaction

---

### `transactionMemo`: `String`

Memo set on the transaction

---

### `transactionFee`: [`Hbar`](reference/Hbar.md)

Fee set on the transaction

---

### `contractFunctionResult`: [`?ContractFunctionResult`](reference/contract/ContractFunctionResult.md)

Result of a [`ContractExecuteTransaction`](reference/contract/ContractExecuteTransaction.md)

---

### `transfers`: [`Transfer[]`](reference/Transfer.md)

Any transfers made in this transaction

**Note**: Includes fee payments

---

### `tokenTransfers`: `Map<TokenId, Map<AccountId, Uint64>>`

Any token transfers made in this transaction

**Note**: These token transfers are different than the ones set in [`TransferTransaction`](reference/cryptocurrency/TransferTransaction.md)

---

### `scheduleRef`: [`ScheduleId`](reference/schedule/ScheduleId.md)

In the record of an internal transaction, the consensus timestamp of the user transaction that spawned it.

---

### `assessedCustomFees`: `List` < [`AssessedCustomFee`](reference/token/AssessedCustomFee.md) >

In the record of an internal transaction, the consensus timestamp of the user transaction that spawned it.

---

### `automaticTokenAssociations`: `List` < [`TokenAssociation`](reference/token/TokenAssociation.md) >

In the record of an internal transaction, the consensus timestamp of the user transaction that spawned it.

---

### `parentConsensusTimestamp`: `Timestamp`

In the record of an internal transaction, the consensus timestamp of the user transaction that spawned it.

---

### `aliasKey`: [`PublicKey`](reference/cryptography/PublicKey.md)

In the record of an internal CryptoCreate transaction triggered by a user transaction with a 
(previously unused) alias, the new account's alias. 

---

### `duplicates`: [`TransactionRecord`](#)

The records of processing all consensus transaction with the same id as the distinguished
record above, in chronological order.

---

### `children`: [`TransactionRecord`](#)

The records of processing all child transaction spawned by the transaction with the given 
top-level id, in consensus order. Always empty if the top-level status is UNKNOWN.

---

### `paidStakingRewards`: [`Transfer`](reference/Transfer.md)

List of accounts with the corresponding staking rewards paid as a result of a transaction.

---
