# `ContractId`

<details>
<summary><b>Declaration</b></summary>

```typescript
class ContractId {
    constructor(num: Uint64);

    constructor(shard: Uint64, realm: Uint64, num: Uint64);

    fromString(str: string): ContractId;

    fromBytes(data: bytes): ContractId;

    fromSolidityAddress(address: string): ContractId;

    /* property */ shard: Uint64;

    /* property */ realm: Uint64;

    /* property */ num: Uint64;

    toBytes(): bytes;

    toString(): string;
}
```

</details>

<details>
<summary><b>Table of Contents</b></summary>



| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor`](#constructor-num-uint64-) | ✅ | ✅ | ✅
| [`fromString`](#fromstring-str-string-contractid) | ✅ | ✅ | ✅
| [`fromBytes`](#frombytes-data-bytes-contractid) | ✅ | ✅ | ✅
| [`fromSolidityAddress`](#fromsolidityaddress-str-string-contractid) | ✅ | ✅ | ✅
| [`shard`](#shard-uint64) | ✅ | ✅ | ✅
| [`realm`](#realm-uint64) | ✅ | ✅ | ✅
| [`num`](#num-uint64) | ✅ | ✅ | ✅
| [`toBytes`](#tobytes-bytes) | ✅ | ✅ | ✅

</details>

An ID type that represents a contract on a Hedera Hashgraph network.

### Constructors

##### `constructor` ( `num` : `Uint64` )

Construct a [`ContractId`](#) with [`shard`](#shard-uint64) and [`realm`](#realm-uint64) being zero.

---

##### `constructor` ( `shard` : `Uint64`, `realm` : `Uint64`, `num` : `Uint64` )

Construct a [`ContractId`](#) with all fields explicitly set.

---

### Static Methods

##### `fromString` ( `str` : `string` ): [`ContractId`](#contractid)

Construct a [`ContractId`](#) from a string. The format of the string could be either just
a number "4" or dot separated numbers "0.0.4".

##### `fromBytes` ( `data` : `bytes` ): [`ContractId`](#contractid)

Deserialize a [`ContractId`](#) from its the protobuf representation.

##### `fromSolidityAddress` ( `str` : `string` ): [`ContractId`](#contractid)

Construct a [`ContractId`](#) a solidity address.

### Methods

##### `toBytes` ( ): `bytes`

Serialize the [`ContractId`](#) into its protobuf representation.

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
