> class `TransactionReceipt`

The summary of a transaction's result so far. If the transaction has not reached consensus, this
result will be necessarily incomplete. 

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): `TransactionReceipt`

Decode a `TransactionReceipt` from an appropriate protobuf encode structure

---

### Methods

##### `toBytes` (): `bytes`

The byte representation of the encoded protobuf type

---

##### `toString` (): `String`

Stringification of all the current values

---

### Fields

##### `status`: [`Status`](reference/Status.md)

Status of the submitted transaction.

---

##### `exchangeRate`: [`ExchangeRate`](reference/ExchangeRate.md)

Current exchange rant for Hbar to USD

---

##### `accountId`: [`AccountId?`](reference/cryptocurrency/AccountId.md)

An account ID

**Note**: Only present if this receipt is for an `AccountCreateTransaction`

---

##### `fileId`: [`FileId?`](reference/file/FileId.md)

A file ID

**Note**: Only present if this receipt is for an `FileCreateTransaction`

---

##### `contractId`: [`ContractId?`](reference/contract/ContractId.md)

A contract ID

**Note**: Only present if this receipt is for an `ContractCreateTransaction`

---

##### `topicId`: [`TopicId?`](reference/consensus/TopicId.md)

A topic ID

**Note**: Only present if this receipt is for an `TopicCreateTransaction`

---

##### `TokenId`: [`TokenId?`](reference/token/TokenId.md)

A token ID

**Note**: Only present if this receipt is for an `TokenCreateTransaction`

---

##### `topicSequenceNumber`: `Uint64`

The current sequence number of the topic

**Note**: Only present if this receipt is for an `TopicMessageSubmitTransaction`

---

##### `topicRunningHash`: `bytes`

The current running hash of the topic

**Note**: Only present if this receipt is for an `TopicMessageSubmitTransaction`

---

##### `totalSypply`: `Uint64`

The total supply of tokens for the current token

**Note**: Only present if this receipt is for an `TopicMessageSubmitTransaction`

---

##### `scheduleId`: [`ScheduleId`](reference/schedule/ScheduleId.md)

In the receipt of a ScheduleCreate, the id of the newly created Scheduled Entity

---

##### `scheduleTransactionId`: [`TransactionId`](reference/core/TransactionId.md)

In the receipt of a ScheduleCreate or ScheduleSign that resolves to SUCCESS, the
TransactionID that should be used to query for the receipt or record of the relevant
scheduled transaction

---

##### `serialNumbers`: `List` < `Int64` >

In the receipt of a TokenMint for tokens of type NON\_FUNGIBLE\_UNIQUE, the serial numbers of
the newly created NFTs

---

### `duplicates`: [`TransactionReceipt`](#)

The receipts of processing all transactions with the given id, in consensus time order.

---

### `children`: [`TransactionReceipt`](#)

The receipts (if any) of all child transactions spawned by the transaction with the 
given top-level id, in consensus order. Always empty if the top-level status is UNKNOWN.

---
