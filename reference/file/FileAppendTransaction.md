# `FileAppendTransaction`

> class `FileAppendTransaction` extends [`Transaction`](reference/core/Transaction.md)

Append contents to a new file that exists on the Hedera Hashgraph network.

When contents that will be appended are larger than 4096 bytes the transaction
will be chunked into several `FileAppendTransaction`'s implicitly. Whenever the
transaction is executed all the chunked transactions will also be executed awaiting
receipt before each successive transaction. This is done to maintain correctness, but
will increase the time needed to execute this transaction. This transaction also
has the `executeAll()` method because it is chunked; this method is not accessible
by all `Transaction` types.

<details>
<summary><b>Declaration</b></summary>

```typescript
class FileAppendTransaction extends Transaction {
    /* property */ fileId?: FileId;

    /* property */ contents?: bytes;

    executeAll(client: Client): TransactionResponse[];
}
```

</details>

<details>
<summary><b>Table of Contents</b></summary>



| Item | Java | JavaScript | Go
| - | - | - | - |
| [`fileId`](#fileid-fileid) | ✅ | ✅ | ✅
| [`contents`](#contents-bytes) | ✅ | ✅ | ✅

</details>

<!-- tabs:start -->

#### ** Java **

```java
var receipt = new FileAppendTransaction()
    .setFileId(fileId)
    .setContents("Append these contents")
    .execute(client) // TransactionResponse
    .getReceipt(client); // TransactionReceipt
```

#### ** JavaScript **

```javascript
const receipt = await (
    await new FileAppendTransaction({
        fileId: fileId,
        contents: "Append these contents",
    }).execute(client)
).getReceipt(client);
```

#### ** Go **

```go
response, err := hedera.NewFileAppendTransaction().
    SetFileID(fileID).
    SetContents([]bytes(transaction))
    Execute(client) // TransactionResponse
if err != nil {
    println(err.Error())
}

receipt, err := response.GetReceipt(client)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Properties

##### `fileId`: [`FileId`](reference/file/FileId.md)

This is the fileID which contents will be appended to.

---

##### `contents`: `bytes`

These are the contents which will be appended to the file.

**Note**. The setter `.setContents()` supports types `bytes` **and** UTF-8 `string`.

---
