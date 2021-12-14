> class `TransactionId`

### Constructor

##### `constructor` ( `accountId`: `AccountId`, `validStart`: `Timestamp` )

Construct a transaction ID from an account ID and a timestamp

---

### Static Methods

##### `generate` ( `accountId`: `AccountId` ): `TransactionId`

Generate a transaction ID with the given account ID and a generated timestamp

---

##### `fromString` ( `text`: `String` ): `TransactionId`

Construct a transaction ID from string

**NOTE**: The transaction ID format is
`(?<accountId>(\d+.\d+)?\d+)\.(?<timestamp>\d+.\d+)(?<scheduled>\?scheduled)?(?<nonce>/\d+)?`

---

##### `fromBytes` ( `data`: `byte[]` ): `TransactionId`

Construct the transaction ID from a protobuf encoded `TransactionID`

---

### Methods

##### `toString` (): `String`

Stringify the transaction ID

---

##### `toBytes` (): `byte[]`

Serialize the tranaction into protobuf encoded bytes

---

### Fields

##### `accountId`: [`AccountId`](reference/AccountId.md)

The account ID of the transaction ID

This account pays for the the transaction

---

##### `validStart`: [`Timestamp`](reference/Timestamp.md)

The timestamp of this transaction

Each transaction ID must have a unique timestamp. Timestamp generation in the SDK fuzzes the current
time so collisions are less likely

---

##### `nonce`: `Uint64`

The identifier for an internal transaction that was spawned as part of handling a user transaction.
(These internal transactions share the transactionValidStart and accountID of the user transaction,
so a nonce is necessary to give them a unique TransactionID.)

An example is when a "parent" ContractCreate or ContractCall transaction calls one or more HTS
precompiled contracts; each of the "child" transactions spawned for a precompile has a id with a
different nonce.

---
