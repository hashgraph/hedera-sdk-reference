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

### `receipt`: [`TransactionReceipt`](reference/core/TransactionReceipt.md)

---

### `transactionHash`: `bytes`

---

### `consensusTimestamp`: `Timestamp`

---

### `transactionId`: [`TransactionId`](reference/core/TransactionId.md)

---

### `transactionMemo`: `String`

---

### `transactionFee`: [`Hbar`](reference/Hbar.md)

---

### `contractFunctionResult`: [`?ContractFunctionResult`](reference/contract/ContractFunctionResult.md)

---

### `transfers`: [`Transfer[]`](reference/Transfer.md)

---

### `tokenTransfers`: `Map<TokenId, Map<AccountId, Uint64>>`

---
