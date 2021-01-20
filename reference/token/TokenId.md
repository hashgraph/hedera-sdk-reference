# `TokenId`

> class `TokenId`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor`](#constructor-num-uint64-) | ✅ | ✅ | ✅
| [`fromString`](#fromstring-str-string-tokenid) | ✅ | ✅ | ✅
| [`fromBytes`](#frombytes-data-bytes-tokenid) | ✅ | ✅ | ✅
| [`shard`](#shard-uint64) | ✅ | ✅ | ✅
| [`realm`](#realm-uint64) | ✅ | ✅ | ✅
| [`num`](#num-uint64) | ✅ | ✅ | ✅
| [`toBytes`](#tobytes-bytes) | ✅ | ✅ | ✅

</details>

An ID type that represents a token on a Hedera Hashgraph network.

### Constructors

##### `constructor` ( `num` : `Uint64` )

Construct a [`TokenId`](#) with [`shard`](#shard-uint64) and [`realm`](#realm-uint64) being zero.

---

##### `constructor` ( `shard` : `Uint64`, `realm` : `Uint64`, `num` : `Uint64` )

Construct a [`TokenId`](#) with all fields explicitly set.

---

### Static Methods

##### `fromString` ( `str` : `String` ): [`TokenId`](#tokenid)

Construct a [`TokenId`](#) from a string. The format of the string could be either just
a number "4" or dot separated numbers "0.0.4".

##### `fromBytes` ( `data` : `bytes` ): [`TokenId`](#tokenid)

Deserialize a [`TokenId`](#) from its the protobuf representation.

### Methods

##### `toBytes` ( ): `bytes`

Serialize the [`TokenId`](#) into its protobuf representation.

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
