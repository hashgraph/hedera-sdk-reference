> class `AddressBookQuery`

<!-- tabs:start -->

### ** Java **

```java
var addressBook = new AddressBookQuery()
    .setFileId(fileId)
    .execute(client);
```

### ** JavaScript **

```javascript
const addressBook = await new AddressBookQuery()
    .setFileId(account)
    .execute(client);
```

### ** Go **

```go
addressBook, err := NewAddressBookQuery().
    SetFileID(fileID).
    Execute(client)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Constructor

##### `constructor`()

---

### Methods

##### `execute` ( `client`: [`Client`](reference/core/Client.md) ): `AddressBook`

Execute this query against a mirror node to get the address book.

---

### Properties

##### `fileId`: [`FileId`](reference/file/FileId.md)

The file ID of the address book to query

**NOTE**: You can use `FileId.ADDRESS_BOOK`

---

##### `limit`: `Uint32?`

Limit the amount of nodes to return. If unset will return entire address book.

---
