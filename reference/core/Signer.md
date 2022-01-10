> abstract class `Signer`

### Methods

##### `async signMessage` ( `messages`: `List` < `bytes` > ): `List` < `List` < `SignerSignature` > >

Sign a list of messages

**NOTE**: Each element in the outer list of the result is all the signatures for the
at the same index.

---

##### `async signTransaction` ( `transaction`: `Transaction` )

Signs the transaction

**NOTE**: Use `Transaction.getSignatures()` to see the actual signatures.
at the same index.

---

##### `async sendTransaction` ( `transaction`: `Transaction` ): `TransactionReceipt`

Sign and send a transaction using the wallet

**NOTE**: Unlike `Provider.sendTransaction()` this method will automatically wait for
the receipt of the transaction.

---

##### `async checkTransaction` ( `transaction`: `Transaction` )

Determines if all the properties requried are set and sets the transaction ID. If the transaction ID was already set it checks if the account ID of it is the same as the users.

---

##### `async populateTransaction` ( `transaction`: `Transaction` )

Sets the transaction ID of the transaction to the current account ID of the signer.

---

##### `getLedgerId` (): `LedgerId`

Return the ledger ID

---

##### `getAccountId` (): `AccountID`

Return the account ID associated with this signer

---

##### `async getAccountBalance` (): `AccountBalance`

Fetch the account's balance

---

##### `async getAccountInfo` (): `AccountInfo`

Fetch the account's info

---

##### `async getTransactionRecords` (): `List` < `TransactionRecord` >

Fetch the last transaction records for this account using `TransactionRecordQuery`

---

##### `async getTransactionRecords` (): `List` < `TransactionRecord` >

Fetch the last transaction records for this account using `TransactionRecordQuery`

---

