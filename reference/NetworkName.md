> class `NetworkName`

Deprecated: Please use [`LedgerId`](reference/LedgerId.md) instead

### Variants

##### MAINNET

The ledger ID for mainnet

##### TESTNET

The ledger ID for testnet

##### PREVIEWNET

The ledger ID for previewnet

##### OTHER

An unrecognized ledger ID

### Static Methods

##### `fromString` ( `networkName`: `string` ): `NetworkName`

Construct a `NetworkName` from a string: `"mainnet"`, `"testnet"`, or `"previewnet"`.

---

### Methods

##### `toString` ( ): `bytes`

Stringify the ledger ID to `"mainnet"`, `"testnet"`, or `"previewnet"`

---
