# `Transaction`

> abstract class `Transaction`

<details>
<summary><b>Declaration</b></summary>

```typescript
abstract class Transaction {
    static fromBytes(data: bytes): Transaction;

    /* property */ nodeAccountId: AccountId;

    /* property */ transactionValidDuration: Duration;

    /* property */ transactionMemo: string;

    /* property */ transactionId: TransactionId;

    /* property */ maxTransactionFee: ?Hbar;

    getTransactionHash(): bytes;

    toBytes(): bytes;

    sign(key: PrivateKey): this;

    signWith(key: PublicKey, transactionSigner: (bytes) => bytes): this;

    signWithOperator(client: Client);

    freeze(): this;

    freezeWith(client: Client): this;

    execute(client: Client): TransactionResponse;
}
```

</details>

Base class for all transactions that may be submitted to Hedera.

### Static Methods

##### `fromBytes` ( `data` : `bytes` ): `Transaction`

---

### Methods

##### `execute` ( `client`: [`Client`](reference/Client.md) ): [`TransactionResponse`](reference/TransactionResponse.md)

Execute this transaction on the Hedera network, immediately returning
metadata about the transaction that was executed. The `TransactionResponse`
may be used to fetch the `TransactionReceipt` or `TransactionRecord`
for more information.

---

##### `toBytes` (): `bytes`

Encodes this transaction to a byte array that can be later decoded into
the same `Transaction`.

---

##### `getTransactionHash` (): `bytes`

---

##### `sign` ( `key`: `PrivateKey` ): `this`

---

##### `signWith` ( `publicKey`: [`PublicKey`](reference/cryptography/PublicKey.md), `transactionSigner`: `(bytes) => bytes` ): `this`

---

##### `signWithOperator` ( `client`: `Client` ): `this`

---

##### `freeze` (): `this`

---

##### `freezeWith` ( `client`: `Client` ): `this`

---

### Properties

##### `nodeAccountId`: [`AccountId`](reference/AccountId.md)

The account ID of the node that this transaction will be submitted to.

Providing an explicit node account ID interferes with client-side load
balancing of the network. By default, the SDK will pre-generate a transaction
for 1/3 of the nodes on the network. If a node is down, busy, or otherwise
reports a fatal error, the SDK will try again with a different node.

---

##### `transactionValidDuration`: `Duration`

Duration from the valid start (within the transaction ID) that this
transaction is valid for.

Defaults to 120 seconds.

---

##### `maxTransactionFee`: `Hbar`

The maximum transaction fee the client is willing to pay.

Defaults to `maxTransactionFee` from the `client`.

---

##### `transactionId`: [`TransactionId`](reference/TransactionId.md)

The ID for this transaction, which includes the payer's
account (the account paying the transaction fee).

If two transactions have the same transactionID, they won't both have an effect

---

##### `transactionMemo`: `string`

Any notes or descriptions that should be put into the record (max length 100).

---
