> class `FileContentsQuery` extends [`Query`](reference/core/Query.md) < `bytes` >

<!-- tabs:start -->

#### ** Java **

```java
var contents = new FileContentsQuery()
    .setFileId(fileId)
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .execute(client);
```

#### ** JavaScript **

```javascript
const contents = await new FileContentsQuery()
    .setFileId(file)
    .setNodeAccountIds([response.nodeId])
    .setMaxQueryPayment(new Hbar(1))
    .execute(client);
```

#### ** Go **

```go
contents, err := NewFileContentsQuery().
    SetFileID(*fileID).
    SetMaxQueryPayment(NewHbar(1)).
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    Execute(client) //[]byte
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

This is the fileID which contents queried for.

---
