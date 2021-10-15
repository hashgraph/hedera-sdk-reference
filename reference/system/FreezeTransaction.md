> class `FreezeTransaction` extends [`Transaction`](reference/core/Transaction.md)

At consensus, sets the consensus time at which the platform should stop creating events and
accepting transactions, and enter a maintenance window.

### Constructor

##### `constructor`()

---

### Properties

##### `startTime`: `Timestamp`

---

##### `endTime`: `Timestamp`

Deprecated with no replacement

---

##### `fileId`: [`FileId`](reference/file/FileId.md)

If set, the file whose contents should be used for a network software update during the maintenance
window.

---

##### `fileHash`: `bytes`

If set, the expected hash of the contents of the update file (used to verify the update).

---

##### `fileHash`: `bytes`

If set, the expected hash of the contents of the update file (used to verify the update).

---

##### `frezeType`: `FreezeType`

If set, the expected hash of the contents of the update file (used to verify the update).

---
