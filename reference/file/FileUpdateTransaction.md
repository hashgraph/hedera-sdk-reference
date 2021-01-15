# `FileUpdateTransaction`

> class `FileUpdateTransaction` extends [`Transaction`](reference/core/Transaction.md)

<details>
<summary><b>Declaration</b></summary>

```typescript
class FileUpdateTransaction extends Transaction {
    /* property */ fileId?: FileId;

    /* property */ keys?: Key[];

    /* property */ contents?: bytes;

    /* property */ expirationTime?: Timestamp;
}
```

</details>

<details>
<summary><b>Table of Contents</b></summary>



| Item | Java | JavaScript | Go
| - | - | - | - |
| [`fileId`](#fileid-fileid) | ✅ | ✅ | ✅
| [`keys`](#keys-key) | ✅ | ✅ | ✅
| [`contents`](#contents-bytes) | ✅ | ✅ | ✅
| [`expirationTime`](#expirationtime-timestamp) | ✅ | ✅ | ✅

</details>

<!-- tabs:start -->

#### ** Java **

```java
var newKey = PrivateKey.generate();

var receipt = new FileUpdateTransaction()
    .setFileId(fileId)
    .setKeys(newKey)
    .setContents("New contents of the file")
    .execute(client) // TransactionResponse
    .sign(newKey)
    .getReceipt(client); // TransactionReceipt
```

#### ** JavaScript **

```javascript
const newKey = PrivateKey.generate();

const transaction = new FileAppendTransaction({
    fileId: fileId,
    keys: [ newKey ],
    contents: "Hello, world",
});

await transaction.sign(newKey) // Sign the transaction with the new key;

const response = await transaction.execute(client) // TransactionResponse;
const receipt = await response.getReceipt(client) // TransactionReceipt;
```

#### ** Go **

```go
response, err := hedera.NewFileUpdateTransaction().
    SetFileID(fileId).
    SetKeys(client.GetOperatorPublicKey())
    Execute(client) // TransactionResponse
if err != nil {
    println(err.Error())
}

receipt, err := response.GetReceipt(client) // TransactionReceipt
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Constructor

##### `constructor`()

---

### Properties

##### `fileId`: [`FileId`](reference/file/FileId.md)

This is the fileID that will be updated.

---

##### `keys`: [`Key`](reference/cryptography/Key.md)[]

These are the new keys of the file. These new keys will be required to sign the
the transactions when mutating the file via [`FileUpdateTransaction`](reference/file/FileUpdateTransaction.md)
or [`FileUpdateTransaction`](reference/file/FileUpdateTransaction.md) transactions.
If no key is provided the file is immutable any the aforementioned transactions will
err with status code [`UNAUTHORIZED`](reference/Status.md#UNAUTHORIZED).

---

##### `contents`: `bytes`

These are the new contents of the file after execution. The contents cannot
exceed ~4096 bytes. Use [`FileAppendTransaction`](refernce/file/FileAppendTransaction.md)
to set larger contents.

**Note**. The setter `.setContents()` supports types `bytes` **and** UTF-8 `string`.
**Note**. The contents will completely override the existing contents of the file.

---

##### `expirationTime`: `Timestamp`

The new expiration time of this file. After this time the file will be deleted. To
prevent file from being deleted another [`FileUpdateTransaction`](reference/file/FileUpdateTransaction.md) must be executed with a new expiration time.

- `Timestmap` is the EPOCH seconds and nanoseconds of a future instant.

---
