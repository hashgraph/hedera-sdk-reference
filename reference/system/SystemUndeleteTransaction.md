> class `SystemUndeleteTransaction` extends [`Transaction`](reference/core/Transaction.md)

Undelete a file or smart contract that was deleted by SystemDelete; requires a Hedera
administrative multisignature. 

<!-- tabs:start -->

#### ** Java **

```java
new SystemUndeleteTransaction()
    .setContractId(new ContractId(10))
    .setExpirationTime(Instant.now())
    .execute(client);

new SystemUndeleteTransaction()
    .setFileId(new FileId(10))
    .setExpirationTime(Instant.now())
    .execute(client);
```

#### ** JavaScript **

```js
await new SystemUndeleteTransaction()
    .setContractId(new ContractId(10))
    .setExpirationTime(Timestamp.generate())
    .execute(client);

await new SystemUndeleteTransaction()
    .setFileId(new FileId(10))
    .setExpirationTime(Timestamp.generate())
    .execute(client);
```

#### ** Go **

```go
response, err = hedera.NewSystemUndeleteTransaction().
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

response, err = hedera.NewSystemUndeleteTransaction().
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

##### `fileId`: [`FileId`](reference/file/FileId.md)

---

##### `contractId`: [`ContractId`](reference/contract/ContractId.md)

---

##### `expirationTime`: `Timestamp`

---

