> class `ContractStateChange`

### Properties

##### `contractId`: [`ContractId`](reference/contract/ContractId.md)

The contract to which the storage changes apply to

---

##### `storageChanges`: `List` < `StorageChange` >

The list of storage changes.

---

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): [`ContractStateChange`](#)

Deserialize a [`ContractStateChange`](#) from its protobuf representation.

---

### Methods

##### `toBytes` ( ): `bytes`

Serialize the [`ContractStateChange`](#) into its protobuf representation.

---
