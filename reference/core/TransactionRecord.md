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
