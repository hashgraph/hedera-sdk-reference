> class `TransactionResponse`

When the client sends the node a transaction of any kind, the node replies with this,
which simply says that the transaction passed the pre-check (so the node will submit it to
the network) or it failed (so it won't). To learn the consensus result, the
client should later obtain a receipt (free), or can buy a more detailed record (not free).

### Methods

##### `getReceipt` ( `client`: [`Client`](Client.md) ): [`TransactionReceipt`](TransactionReceipt.md)

Fetch the receipt for the current transaction ID using the same node account ID

---

##### `getReceiptQuery` (): [`TransactionReceiptQuery`](TransactionReceiptQuery.md)

Create a transaction receipt query for this particular transaction ID and node account ID

---

##### `getRecord` ( `client`: [`Client`](Client.md) ): [`TransactionRecord`](TransactionRecord.md)

Fetch the transaction record for the current transaction ID using the same node account ID

**Note**: Will fetch the receipt first, then fetch the record because fetching the record in a
loop will cost more Hbar.

---

##### `getRecordQuery` (): [`TransactionRecordQuery`](TransactionRecordQuery.md)

Create a transaction record query for this particular transaction ID and node account ID

---

##### `toString` (): `String`

Stringification of all the current values

---

### Fields

##### `nodeId`: [`AccountId`](../cryptocurrency/AccountId.md)

The account ID of the node which the transaction was submitted to

---

##### `transactionHash`: `bytes`

Hash of the transaction

**Note**: Should be the same as the [`TransactionRecord.transactionHash`](TransactionRecord.md#transactionhash--bytes)

---

##### `transactionId`: [`TransactionId`](TransactionId.md)

Transaction ID of the transaction that was submitted
