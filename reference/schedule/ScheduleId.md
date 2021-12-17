> class `ScheduleId`

The ID for an a cryptocurrency schedule

### Constructors

##### `constructor` ( `num` : `Uint64` )

Construct a [`ScheduleId`](#) with [`shard`](#shard-uint64) and [`realm`](#realm-uint64) being zero.

---

##### `constructor` ( `shard` : `Uint64`, `realm` : `Uint64`, `num` : `Uint64` )

Construct a [`ScheduleId`](#) with all fields explicitly set.

---

### Static Methods

##### `fromString` ( `str` : `String` ): [`ScheduleId`](#scheduleid)

Construct an [`ScheduleId`](#) from a string. 
`str` must match `^(0|[1-9]\\d*)\\.(0|[1-9]\\d*)\\.((?:[0-9a-fA-F][0-9a-fA-F])+)$`

---

##### `fromBytes` ( `data` : `bytes` ): [`ScheduleId`](#scheduleid)

Deserialize an schedule ID from its the protobuf representation.

---

##### `fromSolidityAddress` ( `str` : `String` ): [`ScheduleId`](#scheduleid)

Construct an schedule ID from a solidity address.

---

### Methods

##### `toBytes` ( ): `bytes`

Serialize this ID into its protobuf representation.

---

##### `validateChecksum` ( `client` : [`Client`](reference/core/Client.md) ): `void`

Validate the schedule ID's checksum matches the client's network.

Note: The client must contain a network with a known [`NetworkName`](reference/NetworkName.md)

---

##### `getChecksum` ( ): `String`

Get the checksum for this schedule ID if it constructed with one.

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

A nonnegative schedule number unique within its realm

---
