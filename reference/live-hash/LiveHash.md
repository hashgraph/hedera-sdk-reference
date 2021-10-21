# `LiveHash`

The livehash, if present

## Properties

### `accountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The account to which the livehash is attached

---

### `hash`: `bytes`

The SHA-384 hash of a credential or certificate

---

### `keys` [`KeyList`](reference/cryptography/KeyList.md)

A list of keys (primitive or threshold), all of which must sign to attach the livehash to an
account, and any one of which can later delete it.

---

### `duration`: `Duration`

The duration for which the livehash will remain valid

---
