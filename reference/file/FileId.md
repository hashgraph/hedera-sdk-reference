> class `FileId`

An ID type that represents a file on a Hedera Hashgraph network.

### Constructors

##### `constructor` ( `num` : `Uint64` )

Construct a [`FileId`](#) with [`shard`](#shard-uint64) and [`realm`](#realm-uint64) being zero.

---

##### `constructor` ( `shard` : `Uint64`, `realm` : `Uint64`, `num` : `Uint64` )

Construct a [`FileId`](#) with all fields explicitly set.

---

### Static Methods

##### `fromString` ( `str` : `String` ): [`FileId`](#fileid)

Construct a [`FileId`](#) from a string. The format of the string could be either just
a number "4" or dot separated numbers "0.0.4".

##### `fromBytes` ( `data` : `bytes` ): [`FileId`](#fileid)

Deserialize a [`FileId`](#) from its the protobuf representation.

### Methods

##### `toBytes` ( ): `bytes`

Serialize the [`FileId`](#) into its protobuf representation.

---

### Properties

##### `shard`: `Uint64`

The shard of this ID.

---

##### `realm`: `Uint64`

The realm of this ID.

---

##### `num`: `Uint64`

The num of this ID.

---
