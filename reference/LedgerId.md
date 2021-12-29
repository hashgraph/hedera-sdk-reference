> class `LedgerId`

### Static Methods

##### `fromString` ( `ledgerId`: `string` ): `LedgerId`

Construct a ledger ID from a string.

**NOTE**: The string can be either hex encoded bytes or `"mainnet"`, `"testnet"`, 
or `"previewnet"`.

---

##### `fromBytes` ( `bytes`: `bytes` ): `LedgerId`

Construct the ledger ID from bytes directly.

**NOTE**: Using the UTF-8 byte representation of `"mainnet"`, `"testnet"`, 
or `"previewnet"` is **NOT** supported.

---

##### `fromNetworkName` ( `networkName`: [`NetworkName`]() ): `LedgerId`

Convert this `NetworkName` into a `LedgerId`

**NOTE**: If `NetworkName` is `OTHER` this will err.

---

### Methods

##### `isMainnet` ( ): `bool`

Return if this ledger ID represents a mainnet ledger ID.

---

##### `isTestnet` ( ): `bool`

Return if this ledger ID represents a testnet ledger ID.

---

##### `isPreviewnet` ( ): `bool`

Return if this ledger ID represents a previewnet ledger ID.

---

##### `toString` ( ): `bytes`

Stringify the ledger ID

**NOTE**: If the ledger ID is a known value such as `[0]`, `[1]`, `[2]` this method
will instead return `"mainnet"`, `"testnet"`, or `"previewnet"`, otherwise it will
hex encode the bytes.

---

##### `toBytes` ( ): `bytes`

Return the ledger ID bytes

---

##### `toNetworkName` ( ): [`NetworkName`]()

Convert this ledger ID into a `NetworkName`.

**NOTE**: If the ledger ID is not a recognzied ledger ID the resulting
`NetworkName` will be `OTHER`.

---

### Constants

##### `MAINNET`: `LedgerId`

The ledger ID for mainnet

---

##### `TESTNET`: `LedgerId`

The ledger ID for testnet

---

##### `PREVIEWNET`: `LedgerId`

The ledger ID for previewnet

---
