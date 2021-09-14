> class `FileInfoQuery` extends [`Query`](reference/core/Query.md) < [`FileInfo`](reference/file/FileInfo.md) >

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`fileId`](#fileid-fileid) | ✅ | ✅ | ✅

</details>

Query a file's current state.

<!-- tabs:start -->

#### ** Java **

```java
var info = new FileInfoQuery()
    .setFileId(fileId)
    .execute(client) // ByteString
```

#### ** JavaScript **

```javascript
const info = await new FileInfoQuery({ fileId }).execute(client); // Uint8Array
```

#### ** Go **

```go
info, err := hedera.NewFileInfoQuery().
    SetFileID(fileID).
    Execute(client) // []byte
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Properties

##### `fileId`: [`FileId`](reference/file/FileId.md)

This is the file ID for which info will be queried for.

---
