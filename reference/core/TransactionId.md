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
`(?<accountId>(\d+.\d+)?\d+)\.(?<timestamp>\d+.\d+)(?<scheduled>scheduled)?`

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
