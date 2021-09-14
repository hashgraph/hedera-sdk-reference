# `SystemDeleteTransaction`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`FileId`](#fileid-fileidreferencefilefileidmd) | ✅ | ✅ | ✅
| [`ContractId`](#contractid-contractidreferencecontractcontractidmd) | ✅ | ✅ | ✅
| [`ExpirationTime`](#expirationtime-instant) | ✅ | ✅ | ✅
</details>

> class `SystemDeleteTransaction` extends [`Transaction`](reference/core/Transaction.md)

<!-- tabs:start -->

#### ** Java **

```java
new SystemDeleteTransaction()
    .setContractId(new ContractId(10))
    .setExpirationTime(Instant.now())
    .execute(client);

new SystemDeleteTransaction()
    .setFileId(new FileId(10))
    .setExpirationTime(Instant.now())
    .execute(client);
```

#### ** JavaScript **

```js
await new SystemDeleteTransaction()
    .setContractId(new ContractId(10))
    .setExpirationTime(Timestamp.generate())
    .execute(client);

await new SystemDeleteTransaction()
    .setFileId(new FileId(10))
    .setExpirationTime(Timestamp.generate())
    .execute(client);
```

#### ** Go **

```go
response, err = hedera.NewSystemDeleteTransaction().
    SetFileID(FileIDFromString("0.0.3").
    SetExpirationTime(time.Now().Local().Add(time.Second * 5)).
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
    SetExpirationTime(time.Now().Local().Add(time.Second * 5)).
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

##### `ExpirationTime`: `Timestamp`

---

