> class `AccountId`

The ID for a cryptocurrency account

### Constructors

##### `constructor` ( `num` : `Uint64` )

Construct a [`AccountId`](AccountId.md) with [`shard`](#shard--uint64) and [`realm`](#realm--uint64) being zero.

---

##### `constructor` ( `shard` : `Uint64`, `realm` : `Uint64`, `num` : `Uint64` )

Construct a [`AccountId`](AccountId.md) with all fields explicitly set.

---

### Static Methods

##### `fromBytes` ( `data` : `bytes` ): [`AccountId`](AccountId.md)

Deserialize an account ID from its protobuf representation.

---

##### `fromEvmAddress` ( `evmAddress` : [`EvmAddress`](EvmAddress.md) ): [`AccountId`](AccountId.md)

Retrieve the account id from an EVM address.

---

##### `fromSolidityAddress` ( `str` : `String` ): [`AccountId`](AccountId.md)

Construct an account ID from a solidity address.

---

##### `fromString` ( `str` : `String` ): [`AccountId`](AccountId.md)

Construct an [`AccountId`](AccountId.md) from a string.
`str` must match `^(0|[1-9]\\d*)\\.(0|[1-9]\\d*)\\.((?:[0-9a-fA-F][0-9a-fA-F])+)$`

### Methods

##### `getChecksum` ( ): `String`

Get the checksum for this account ID if it constructed with one.

---

##### `toBytes` ( ): `bytes`

Serialize this ID into its protobuf representation.

---

##### `toSolidityAddress` ( ): `String`

Extract the solidity address.

---

##### `toString` ( ): `String`

Stringify this ID into `{shard}.{realm}.{num}`

---

##### `toStringWithChecksum` ( `client` : [`Client`](../core/Client.md) ): `String`

Stringify this ID into `{shard}.{realm}.{num}-{checksum}` using the client's network.

Note: The client must contain a network with a known [`NetworkName`](../NetworkName.md)

Note: If the account ID has an `aliasKey`, `toStringWithChecksum` will throw an error

---

##### `validateChecksum` ( `client` : [`Client`](../core/Client.md) ): `void`

Validate the account ID's checksum matches the client's network.

Note: The client must contain a network with a known [`NetworkName`](../NetworkName.md)

Note: If the account ID has an `aliasKey`, `validateChecksum` will throw an error

### Properties

##### `aliasKey`: `PublicKey`

An alias for the `num` of the account if the account was created from a public key directly.

---

##### `evmAddress`: [`EvmAddress`](EvmAddress.md)

The EOA 20-byte address to create that is derived from the keccak-256 hash of a ECDSA_SECP256K1 primitive key.

---

##### `num`: `Uint64`

A non-negative account number unique within its realm

---

##### `realm`: `Uint64`

The realm number (non-negative)

---

##### `shard`: `Uint64`

The shard number (non-negative)
