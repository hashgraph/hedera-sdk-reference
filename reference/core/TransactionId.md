> class `TransactionId`

The client-generated ID for a transaction.

<!-- tabs:start -->

### ** Java **

```java
// create from..
var transactionId = TransactionId.fromString("0.0.23847@1588539964.632521325");
var transactionId = new TransactionId(new AccountId(23847), Instant.ofEpochSecond(1588539964);
```

### ** JavaScript **

```javascript
// create from..
const transactionId = TransactionId.fromString("0.0.23847@1588539964.632521325")
const transactionId = new TransactionId(new AccountId(0, 0, 23847), new Timestamp(1588539964, 4);
```

### ** Go **

```go
// create from..
txID, err := TransactionIdFromString("0.0.23847@1588539964.632521325")
txID := NewTransactionIDWithValidStart(AccountID{Account: 23847}, time.Unix(1588539964, 4))
```

<!-- tabs:end -->

### Constructor

##### `constructor` ( [`AccoundId`](../cryptocurrency/AccountId.md), `validStart`: `Timestamp` )

Construct a transaction ID from an account ID and a timestamp

---

### Static Methods

##### `fromBytes` ( `data`: `byte[]` ): `TransactionId`

Construct the transaction ID from a protobuf encoded `TransactionID`

---

##### `fromString` ( `text`: `String` ): `TransactionId`

Construct a transaction ID from string

**NOTE**: The transaction ID format is
`(?<accountId>(\d+.\d+)?\d+)\.(?<timestamp>\d+.\d+)(?<scheduled>\?scheduled)?(?<nonce>/\d+)?`

---

##### `generate` ( [`AccoundId`](../cryptocurrency/AccountId.md) ): `TransactionId`

Generate a transaction ID with the given account ID and a generated timestamp

---

##### `getReceipt` ( [`Client`](Client.md) ): [`TransactionReceipt`](TransactionReceipt.md)`

Fetch the receipt of the transaction.

---

##### `getRecord` ( [`Client`](Client.md) ): [`TransactionRecord`](TransactionRecord.md)`

Fetch the record of the transaction.

---

##### `withValidStart` ( [`AccoundId`](../cryptocurrency/AccountId.md), `validStart`: `Timestamp` ): `TransactionId`

Create a transaction id.

---

### Methods

##### `toString` (): `String`

Stringify the transaction ID

---

##### `toStringWithChecksum` ( [`Client`](Client.md) ): `String`

Convert to a string representation with checksum

---

##### `toBytes` (): `byte[]`

Serialize the transaction into protobuf encoded bytes

---

### Fields

##### `accountId`: [`AccoundId`](../cryptocurrency/AccountId.md)

The account ID of the transaction ID

This account pays for the transaction

---

##### `nonce`: `Uint64`

The identifier for an internal transaction that was spawned as part of handling a user transaction.
(These internal transactions share the transactionValidStart and accountID of the user transaction,
so a nonce is necessary to give them a unique TransactionID.)

An example is when a "parent" ContractCreate or ContractCall transaction calls one or more HTS
precompiled contracts; each of the "child" transactions spawned for a precompiled contracts has an id with a
different nonce.

---

##### `scheduled`: `bool`

The scheduled status of the transaction

---

##### `validStart`: `Timestamp`

The timestamp of this transaction

Each transaction ID must have a unique timestamp. Timestamp generation in the SDK fuzzes the current
time so collisions are less likely
