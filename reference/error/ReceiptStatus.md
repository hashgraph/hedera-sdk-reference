> error `ReceiptStatus` extends `Error`

### Fields

##### `transactionId`: [`TransactionId`](reference/core/TransactionId.md)

The ID of the transaction that failed, in case that context is no longer available (e.g. the
exception was bubbled up).

---

##### `receipt`: [`TransactionReceipt`](reference/core/TransactionReceipt.md)

The receipt of the transaction that failed; the only initialized field is [`TransactionReceipt.status`](reference/core/TransactionReceipt.md#status-status)

---
