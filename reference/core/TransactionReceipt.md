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
