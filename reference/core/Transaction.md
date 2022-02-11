> abstract class `Transaction` extends [`Executable`](reference/core/Exectuable.md) <
> [`TransactionResponse`](reference/core/TransactionResponse.md) >

Base class for all transactions that may be submitted to Hedera.

### Static Methods

##### `fromBytes` ( `data` : `bytes` ): `Transaction`

Construct a transaction from bytes

**NOTE**: The bytes can be a protobuf encoded `TransactionBody`, `Transaction`, `SignedTransaction`
or `TransactionList`

---

### Methods

##### `execute` ( `client`: [`Client`](reference/core/Client.md) ): [`TransactionResponse`](reference/core/TransactionResponse.md)

Execute this transaction on the Hedera network, immediately returning
metadata about the transaction that was executed.
The [`TransactionResponse`](reference/core/TransactionResponse.md) may be used to fetch
the [`TransactionReceipt`](reference/core/TransactionReceipt.md) or
[`TransactionRecord`](reference/core/TransactionRecord.md)
for more information.

---

##### `toBytes` (): `bytes`

Encodes this transaction to a byte array that can be later decoded into
the same `Transaction`

---

##### `getTransactionHash` (): `bytes`

Generate the SHA-384 hash of the transaction

**NOTE**: Requires a single node account ID to be set on the transaction.
Use `getTransactionHashPerNode()` when node account IDs were not manually set or were set to muliple
values

---

##### `getTransactionHashPerNode()`: `Map` < [`AccoundId`](reference/cryptocurrency/AccountId.md), `bytes` >

Generate the SHA-384 hash of the transaction per node account ID

The key for the returned map is the node account ID

---

##### `sign` ( `key`: [`PrivateKey`](reference/cryptography/PrivateKey.md) ): `Transaction`

Sign the transation with the given private key.

**NOTE**:Signing with the same private key will be ignored.

---

##### `signWith` ( `publicKey`: [`PublicKey`](reference/cryptography/PublicKey.md), `transactionSigner`: `(bytes) => bytes` ): `Transaction`

Sign the transaction with a public key and a signing callback.

**NOTE**:Signing with the same public key will be ignored.

---

##### `signWithOperator` ( `client`: [`Client`](reference/core/Client.md) ): `Transaction`

Sign with the client's operator

**NOTE**: If the operator has already signed this will be ignored

---

##### `freeze` (): `Transaction`

Freeze the transaction getting it ready to be signed or executed.

Freezing without a client requires a transaction ID and node account IDs to be manually set

**NOTE**: Freezing the transaction means it cannot be modified anymore, so make sure to set all the
fields correctly before freezing.

**NOTE**: Freezing is required for certain operations such as signing and generating hash.

---

##### `freezeWith` ( `client`: [`Client`](reference/core/Client.md) ): `Transaction`

Freeze the transaction with a client.

The client's operator will be used to generate a transaction ID, and the client's network will be
used to generate a list of node account IDs

---

##### `getSignatures()`: `Map` < [`AccoundId`](reference/cryptocurrency/AccountId.md), `Map` < [`PublicKey`](reference/cryptography/PublicKey.md), `bytes` >

Get the transaction signatures

---

##### `addSignature`(`key`: [`PublicKey`](reference/cryptography/PublicKey.md), `signature`: `byte[]`): `Transaction`

Add a signature to the transaction

**NOTE**: Requires the transaction to have a single node account ID set

---

### Properties

##### `nodeAccountIds`: [`AccountId[]`](reference/cryptocurrency/AccountId.md)

The list of node account IDs that this transaction will be submitted to.

Providing an explicit set of node account IDs interferes with client-side load balancing of the
network. By default, the SDK will pre-generate a transaction for 1/3 of the nodes on the network. If
a node is down, busy, or otherwise reports a fatal error, the SDK will try again with a different
node.

---

##### `transactionValidDuration`: `Duration`

Duration from the valid start (within the transaction ID) that this
transaction is valid for.

Defaults to 120 seconds.

---

##### `maxTransactionFee`: [`Hbar`](reference/Hbar.md)

The maximum transaction fee the client is willing to pay.

Defaults to `maxTransactionFee` from the `client`.

---

##### **Read-Only** `defaultMaxTransactionFee`: [`Hbar`](reference/Hbar.md)

Get the default max transaction fee set for this transaction.

This value is set by the SDK

---

##### `transactionId`: [`TransactionId`](reference/core/TransactionId.md)

The ID for this transaction, which includes the payer's account (the account paying the transaction
fee).

If two transactions have the same transactionID, they won't both have an effect

---

##### `transactionMemo`: `String`

Any notes or descriptions that should be put into the record (max length 100).

---

##### `maxAttempts`: `Uint64`

The number of times to retry submitting this transaction. Transactions are retried when Hedera
Hashgraph returns a status code that implies the transaction should be resubmitted, or when a node
doesn't respond.

---

##### `regenerateTransactionId`: `bool`

Declares if we should generate new transaction IDs when a transaction fails with
`TRANSACTION_EXPIRED`

**NOTE**: Defaults to `true`

**NOTE**: If transaction IDs are locked, this option is ignored. Transaction IDs can be
locked if set manually or if certain methods are called.

---

##### `operatorAccountId`: [`?AccountId`](reference/cryptocurrency/AccountId.md)

The operator account ID to use for this transaction

**NOTE**: If one is not set, the first operator in the `Client` will be used

---
