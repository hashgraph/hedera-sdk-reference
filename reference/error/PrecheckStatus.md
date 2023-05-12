> class `PrecheckStatusError` extends `Error`

Signals that a transaction has failed the pre-check. Before a node submits a transaction to the rest
of the network, it attempts some cheap assertions. This process is called the "pre-check".

### Fields

##### `status`: [`Status`](../Status.md)

The status of the failing transaction

---

##### `transactionId`: [`TransactionId`](../core/TransactionId.md)

The ID of the transaction that failed. This can be `null` if a query fails pre-check without an
associated payment transaction.
