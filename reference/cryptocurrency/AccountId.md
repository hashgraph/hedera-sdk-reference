> class `AccountId`

The ID for an a cryptocurrency account

### Constructors

##### `constructor` ( `num` : `Uint64` )

Construct a [`AccountId`](#) with [`shard`](#shard-uint64) and [`realm`](#realm-uint64) being zero.

---

##### `constructor` ( `shard` : `Uint64`, `realm` : `Uint64`, `num` : `Uint64` )

Construct a [`AccountId`](#) with all fields explicitly set.

---

### Static Methods

##### `fromString` ( `str` : `String` ): [`AccountId`](#accountid)

Construct an [`AccountId`](#) from a string. The format of the string could be either just
a number "4" or dot separated numbers "0.0.4".

---

##### `fromBytes` ( `data` : `bytes` ): [`AccountId`](#accountid)

Deserialize an account ID from its the protobuf representation.

---

##### `fromSolidityAddress` ( `str` : `String` ): [`AccountId`](#accountid)

Construct an account ID from a solidity address.

---

### Methods

##### `toBytes` ( ): `bytes`

Serialize this ID into its protobuf representation.

---

##### `validateChecksum` ( `client` : [`Client`](reference/core/Client.md) ): `void`

Validate the account ID's checksum matches the client's network.

Note: The client must contain a network with a known [`NetworkName`](reference/NetworkName.md)

---

##### `getChecksum` ( ): `String`

Get the checksum for this account ID if it constructed with one.

---

##### `toString` ( ): `String`

Stringify this ID into `{shard}.{realm}.{num}`

---

##### `toStringWithChecksum` ( `client` : [`Client`](reference/core/Client.md) ): `String`

Stringify this ID into `{shard}.{realm}.{num}-{checksum}` using the client's network.

Note: The client must contain a network with a known [`NetworkName`](reference/NetworkName.md)

---

### Properties

##### `shard`: `Uint64`

The shard number (nonnegative)

---

##### `realm`: `Uint64`

The realm number (nonnegative)

---

##### `num`: `Uint64`

A nonnegative account number unique within its realm

---
