> class `FileInfo`

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): [`FileInfo`](#)

Deserialize a [`FileInfo`](#) from its protobuf representation.

---

### Methods

##### `toBytes` ( ): `bytes`

Serialize the [`FileInfo`](#) into its protobuf representation.

---

### Properties

### `fileId` : [`FileId`](reference/file/FileId.md)

The ID for which this info belongs to.

---

### `size` : `Uint64`

The length of this file's contents.

---

### `expirationTime` : `Timestamp`

The expiration time of this file. When current time surpasses the expiration time the
file is deleted from the network. To update the expiration time use [`FileUpdateTransaction`](reference/file/FileUpdateTransaction.md).

---

### `isDeleted` : `boolean`

Identifies if this file has been deleted.

---

### `keys` : [`KeyList`](reference/cryptography/KeyList.md)

The keys that are required to sign transactions that mutate this file.

---

##### `ledgerId`: [`LedgerId`](reference/LedgerId.md)

The ID of the ledger which returned this response

---
