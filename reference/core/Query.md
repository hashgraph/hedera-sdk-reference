> abstract class `Query` < `O` > extends [`Executable`](Exectuable.md) < `0` >

Base class for all queries that may be submitted to Hedera.

### Methods

##### `execute` ( `client`: [`Client`](Client.md) ): `O`

Execute this query on the chosen Hedera network node and return its response.

The return type of this method is dictated by the derived class.

---

##### `getCost` ( `client`: [`Client`](Client.md) ): [`Hbar`](../Hbar.md)

Return the cost to execute this query on the chosen Hedera network node.

---

### Properties

##### `maxAttempts`: `Uint32`

The number of times to retry submitting this transaction. Transactions are retried when Hedera
Hashgraph returns a status code that implies the transaction should be resubmitted, or when a node
doesn't respond.

---

##### `maxBackoff`: `Duration`

The maximum amount of time to wait between retries

---

##### **Write-only** `maxQueryPayment`: [`?Hbar`](../Hbar.md)

The maximum query payment the client is willing to pay.

Defaults to `maxQueryPayment` from the `client`.

---

##### `minBackoff`: `Duration`

The minimum amount of time to wait between retries

---

##### `nodeAccountIds`: [`AccountId[]`](../cryptocurrency/AccountId.md)

The node account IDs that will be queried.

---

##### `paymentTransactionId`: [`TransactionId`](TransactionId.md)

The transaction ID

---

##### **Write-only** `queryPayment`: [`Hbar?`](../Hbar.md)

The exact query payment the client will pay for this query.

If not set, the cost will be dynamically fetched from the network and used (
respecting the `maxQueryPayment` setting).
