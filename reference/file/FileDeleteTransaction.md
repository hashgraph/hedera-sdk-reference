# `FileDeleteTransaction`

> class `FileDeleteTransaction` extends [`Transaction`](reference/core/Transaction.md)

Delete a file that exists on the Hedera Hashgraph network.

<details>
<summary><b>Declaration</b></summary>

```typescript
class FileDeleteTransaction extends Transaction {
    /* property */ fileId?: FileId;
}
```

</details>

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`fileId`](#fileid-fileid) | ✅ | ✅ | ✅

</details>

<!-- tabs:start -->

#### ** Java **

```java
var receipt = new FileDeleteTransaction()
    .setFileId(fileId)
    .execute(client) // TransactionResponse
    .getReceipt(client); // TransactionReceipt
```

#### ** JavaScript **

```javascript
const receipt = await (
    await new FileDeleteTransaction({ fileId }).execute(client)
).getReceipt(client);
```

#### ** Go **

```go
response, err := NewFileDeleteTransaction().
    SetFileID(fileID).
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

### Constructor

##### `constructor`()

---

### Properties

##### `fileId`: [`FileId`](reference/file/FileId.md)

This is the ID of the file to delete.

---
