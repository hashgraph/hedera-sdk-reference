# `SystemUndeleteTransaction`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`FileId`](#fileid-fileidreferencefilefileidmd) | ✅ | ✅ | ✅
| [`ContractId`](#contractid-contractidreferencecontractcontractidmd) | ✅ | ✅ | ✅
</details>

> class `SystemUndeleteTransaction` extends [`Transaction`](reference/core/Transaction.md)

<!-- tabs:start -->

#### ** Java **

```java
new SystemUndeleteTransaction()
    .setContractId(new ContractId(10))
    .execute(client);

new SystemUndeleteTransaction()
    .setFileId(new FileId(10))
    .execute(client);
```

#### ** JavaScript **

```js
await new SystemUndeleteTransaction()
    .setContractId(new ContractId(10))
    .execute(client);

await new SystemUndeleteTransaction()
    .setFileId(new FileId(10))
    .execute(client);
```

#### ** Go **

```go
response, err = hedera.NewSystemDeleteTransaction().
    SetFileID(FileIDFromString("0.0.3").
    SetNodeAccountIDs([]AccountID{response.NodeID}).
    Execute(client)
if err != nil {
    println(err.Error())
}

receipt, err := response.GetReceipt(client)
if err != nil {
    println(err.Error())
}

response, err = hedera.NewSystemDeleteTransaction().
    SetContractID(ContractIDFromString("0.0.3").
    SetNodeAccountIDs([]AccountID{response.NodeID}).
    Execute(client)
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

##### `FileId`: [`FileId`](reference/file/FileId.md)

---

##### `ContractId`: [`ContractId`](reference/contract/ContractId.md)

---
