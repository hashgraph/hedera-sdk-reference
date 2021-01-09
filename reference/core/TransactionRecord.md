# `TransactionRecord`

> class `TransactionRecord`

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): `TransactionRecord`

---

### Methods

##### `toBytes` (): `bytes`

---

##### `toString` (): `String`

---

### Fields

### `receipt`: [`TransactionReceipt`](reference/core/TransactionRecord.md)

---

### `transactionHash`: `bytes`

---

### `consensusTimestamp`: `Timestamp`

---

### `transactionId`: [`TransactionId`](reference/core/TransactionId.md)

---

### `transactionMemo`: `string`

---

### `transactionFee`: `Hbar`

---

### `contractFunctionResult`: [`?ContractFunctionResult`](reference/contract/ContractFunctionResult.md)

---

### `transfers`: [`Transfer[]`](reference/Transfer.md)

---

### `tokenTransfers`: `Map<TokenId, Map<AccountId, Uint64>>`

---
