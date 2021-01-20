> class `ContractLogInfo`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`contractId`](#contractid-contractid) | ✅ | ✅ | ✅
| [`bloom`](#bloom-bytes) | ✅ | ✅ | ✅
| [`topics`](#topics-bytes) | ✅ | ✅ | ✅
| [`data`](#data-bytes) | ✅ | ✅ | ✅
| [`toBytes`](#tobytes-bytes) | ✅ | ✅ | ✅
| [`fromBytes`](#frombytes-data-bytes-contractloginfo) | ✅ | ✅ | ✅

</details>

### Properties

##### `contractId`: [`ContractId`](reference/contract/ContractId.md)

---

##### `bloom`: `bytes`

---

##### `topics`: `bytes`

---

##### `data`: `bytes`

---

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): [`ContractLogInfo`](#)

Deserialize a [`ContractLogInfo`](#) from its protobuf representation.

---

### Methods

##### `toBytes` ( ): `bytes`

Serialize the [`ContractLogInfo`](#) into its protobuf representation.

---
