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

Construct an [`AccountId`](#) from a string. 
`str` must match `^(0|[1-9]\\d*)\\.(0|[1-9]\\d*)\\.((?:[0-9a-fA-F][0-9a-fA-F])+)$`

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

Note: If the account ID has an `aliasKey`, `validateChecksum` will throw an error 

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

Note: If the account ID has an `aliasKey`, `toStringWithChecksum` will throw an error 

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

##### `aliasKey`: `PublicKey`

An alias for the `num` of the account if the account was created from a public key directly.

---

##### `evmAddress`: `Bytes`

The EOA 20-byte address to create that is derived from the keccak-256 hash of a ECDSA_SECP256K1 primitive key.

---
