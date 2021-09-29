> class `ClientConfig`

The config file specification for [`Client`](reference/core/Client.md) construction

### Properties

##### `newtork` : `Map` < `String` , `String` >

The custom network map

The key is the address and the value is the serialized form of
[`AccountId`](reference/cryptocurrency/AccountId.md)

---

##### `newtork` : `String` 

The name of the network

Valid values are "previewnet", "testnet", or "mainnet"

---

##### `mirrorNetwork` : `List` < `String` >

The custom mirror network list

Each value in the list is the address to a mirror node

---

##### `mirrorNetwork` : `String` 

The name of the mirror network

Valid values are "previewnet", "testnet", or "mainnet"

---

##### `operator` : [`Operator`](reference/core/OperatorConfig.md) 

The operator for the given client

---

##### `networkName` : `String`

Set the name of the given network.

Useful when `network` is a custom network map

---
