> class `TransactionId`

### Constructor

##### `constructor` ( `accountId`: `AccountId`, `validStart`: `Timestamp` )

---

### Static Methods

##### `generate` ( `accountId`: `AccountId` ): `TransactionId`

---

##### `fromString` ( `text`: `String` ): `TransactionId`

---

##### `fromBytes` ( `data`: `byte[]` ): `TransactionId`

---

### Methods

##### `toString` (): `String`

---

##### `toBytes` (): `byte[]`

---

##### `equals` (`id` : `TransactionId`): `bool`

---

##### `hashCode` (): `int`

---

### Fields

##### `accountId`: [`AccountId`](reference/AccountId.md)

---

##### `validStart`: [`Timestamp`](reference/Timestamp.md)

---
