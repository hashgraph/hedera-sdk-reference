> abstract class `Provider`

### Methods

##### `getLedgerId` (): `LedgerId`

Return the ID of the current network

---

##### `async getAccountBalance` ( `accountId`: `AccountId` ): `AccountBalance`

Get the balance for an account

---

##### `async getAccountInfo` ( `accountId`: `AccountId` ): `AccountInfo`

Get the info for an account

---

##### `async getTransactionReceipt` ( `transactionId`: `TransactionId` ): `TransacitonReceipt`

Get a receipt for a transaction ID

---

##### `async sendTransaction` ( `transaction`: `Transaction` ): `TransactionResponse`

Sign and send a transaction using the wallet

---

##### `async waitForReceipt` ( `response`: `TransactionResponse` ): `TransactionReceipt`

Wait for the receipt for a transaction response

**NOTE**: This is different than `getTransactionReceipt()` this method requires a `nodeId` which
is set inside `TransactionResponse` and as a result should not be able to fail with `RECEIPT_NOT_FOUND`

---

