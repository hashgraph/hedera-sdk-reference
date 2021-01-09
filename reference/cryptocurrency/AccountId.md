# `AccountId`

> class `AccountId`

### Constructor

##### `constructor` ( `num`: `Uint64` )

---

##### `constructor` ( `shard`: `Uint64`, `realm`: `Uint64`, `num`: `Uint64` )

---

### Static Methods

##### `fromString` ( `text` : `string` ): `AccountId`

---

##### `fromSolidityAddress` ( `address`: `string` ): `AccountId`

---

##### `fromBytes` ( `byte`: `byte[]` ): `AccountId`

---

### Methods

##### `toString` (): `string`

---

##### `toSolidityAddress` (): `string`

---

##### `equals` ( `other`: `AccountId` ): `bool`

---

##### `hashCode` (): `int`

---

##### `toBytes` (): `byte[]`

---

### Fields

##### `shard`: `Uint64`

---

##### `realm`: `Uint64`

---

##### `num`: `Uint64`

---
