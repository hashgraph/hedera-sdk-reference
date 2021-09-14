> class `FileInfo`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`fromBytes`](#frombytes-data-bytes-fileinfo) | ✅ | ✅ | ✅
| [`fileId`](#fileid-fileid) | ✅ | ✅ | ✅
| [`size`](#size-uint64) | ✅ | ✅ | ✅
| [`expirationTime`](#expirationtime-timestamp) | ✅ | ✅ | ✅
| [`deleted`](#isdeleted-boolean) | ✅ | ✅ | ✅
| [`keys`](#keys-keylist) | ✅ | ✅ | ✅
| [`toBytes`](#tobytes-bytes) | ✅ | ✅ | ✅

</details>


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

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): [`FileInfo`](#)

Deserialize a [`FileInfo`](#) from its protobuf representation.

---

### Methods

##### `toBytes` ( ): `bytes`

Serialize the [`FileInfo`](#) into its protobuf representation.

---
