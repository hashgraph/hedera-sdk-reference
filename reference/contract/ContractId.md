> class `ContractId` implements [`Key`](reference/cryptography/Key.md)

An ID type that represents a contract on a Hedera Hashgraph network.

### Constructors

##### `constructor` ( `num` : `Uint64` )

Construct a [`ContractId`](#) with [`shard`](#shard-uint64) and [`realm`](#realm-uint64) being zero.

---

##### `constructor` ( `shard` : `Uint64`, `realm` : `Uint64`, `num` : `Uint64` )

Construct a [`ContractId`](#) with all fields explicitly set.

---

### Static Methods

##### `fromString` ( `str` : `String` ): [`ContractId`](#contractid)

Construct a [`ContractId`](#) from a string. The format of the string could be either just
a number "4" or dot separated numbers "0.0.4".

---

##### `fromBytes` ( `data` : `bytes` ): [`ContractId`](#contractid)

Deserialize a [`ContractId`](#) from its the protobuf representation.

---

##### `fromSolidityAddress` ( `str` : `String` ): [`ContractId`](#contractid)

Construct a [`ContractId`](#) a solidity address.

Deprecated: Use `fromEvmAddress()` instead.

---

##### `fromEvmAddress` ( `shard` : `Uint64`, `realm` : `Uint64`, `evmAddress` : `string` ): [`ContractId`](#contractid)

Construct a [`ContractId`](#) from a shard, realm, and evm address.

---

### Methods

##### `toBytes` ( ): `bytes`

Serialize the [`ContractId`](#) into its protobuf representation.

---

##### `toString` ( ): `string`

Serialize the [`ContractId`](#) into a string form which follows `{shard}.{realm}.{num}` if `evmAddress` is not present
and `{shard}.{realm}.{evmAddress}` if `evmAddress` is present.

---

##### `toSolidityAddress` ( ): `string`

Serialize the [`ContractId`](#) into its solidity address form.

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

##### `evmAddress`: `bytes?`

The evm address of this contract.

Note: This field is only set when `fromEvmAddress()` is used. `fromSolidityAddress()` does not populate this field

---
