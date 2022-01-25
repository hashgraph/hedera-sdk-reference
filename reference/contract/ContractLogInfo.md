> class `ContractLogInfo`

### Properties

##### `contractId`: [`ContractId`](reference/contract/ContractId.md)

Address of a contract that emitted the event

---

##### `bloom`: `bytes`

Bloom filter for a particular log

---

##### `topics`: `bytes`

Topics of a particular event

---

##### `data`: `bytes`

Event data

---

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): [`ContractLogInfo`](#)

Deserialize a [`ContractLogInfo`](#) from its protobuf representation.

---

### Methods

##### `toBytes` ( ): `bytes`

Serialize the [`ContractLogInfo`](#) into its protobuf representation.

---
