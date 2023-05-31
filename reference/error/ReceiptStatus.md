> error `ReceiptStatus` extends `Error`

An Exception thrown on error status by [`TransactionId.getReceipt()`](../core/TransactionId.md#getreceipt--client---transactionreceipt-)

### Fields

##### `receipt`: [`TransactionReceipt`](../core/TransactionReceipt.md)

The receipt of the transaction that failed; the only initialized field is [`TransactionReceipt.status`](../core/TransactionReceipt.md#status--status)

---

##### `transactionId`: [`TransactionId`](../core/TransactionId.md)

The ID of the transaction that failed, in case that context is no longer available (e.g. the
exception was bubbled up).
