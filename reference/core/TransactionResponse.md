> class `TransactionResponse`

### Methods

##### `getReceipt` ( `client`: [`Client`](reference/core/Client.md) ): [`TransactionReceipt`](reference/core/TransactionReceipt.md)

Fetch the receipt for the current transaction ID using the same node account ID

---

##### `getRecord` ( `client`: [`Client`](reference/core/Client.md) ): [`TransactionRecord`](reference/core/TransactionRecord.md)

Fetch the transaction record for the current transaction ID using the same node account ID

**Note**: Will fetch the receipt first, then fetch the record because fetching the record in a
loop will cost more hbars.

---

##### `getReceiptQuery` (): [`TransactionReceiptQuery`](reference/core/TransactionReceiptQuery.md)

Create a transaction receipt query for this particular transaction ID and node account ID

---

##### `getRecordQuery` (): [`TransactionRecordQuery`](reference/core/TransactionRecordQuery.md)

Create a transaction record query for this particular transaction ID and node account ID

---

##### `toString` (): `String`

Stringification of all the current values

---


### Fields

##### `nodeAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The account ID of the node which the transaction was submitted to

---

##### `transactionHash`: `bytes`

Hash of the transaction

**Note**: Should be the same as the [`TransactionRecord.transactionHash`](reference/core/TransactionRecord.md#transactionHash-bytes)

---

##### `transactionId`: [`TransactionId`](reference/core/TransactionId.md)

Transaction ID of the transaction that was submitted

---
