# `FileContentsQuery`

> class `FileContentsQuery` extends [`Query`](reference/core/Query.md) < `bytes` >

<details>
<summary><b>Declaration</b></summary>

```typescript
class FileContentsQuery extends Query<bytes> {
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
var contents = new FileContentsQuery()
    .setFileId(fileId)
    .execute(client) // ByteString
```

#### ** JavaScript **

```javascript
const contents = await new FileContentsQuery({ fileId }).execute(client); // Uint8Array
```

#### ** Go **

```go
contents, err := NewFileContentsQuery().
    SetFileID(fileID).
    Execute(client) // []byte
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Properties

##### `fileId`: [`FileId`](reference/file/FileId.md)

This is the fileID which contents queried for.

---
