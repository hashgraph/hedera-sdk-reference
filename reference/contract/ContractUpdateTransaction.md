# `ContractUpdateTransaction`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`ContractId`](#contractid-Contractid) | ✅ | ✅ | ✅
| [`ContractMemo`](#contractmemo-string) | ✅ | ✅ | ✅
| [`AdminKey`](#adminkey-key) | ✅ | ✅ | ✅
| [`ExpirationTime`](#expirationtime-instant) | ✅ | ✅ | ✅
| [`AutoRenewPeriod`](#autorenewperiod-duration) | ✅ | ✅ | ✅
| [`ProxyAccountId`](#proxyaccountid-accountidreferencecryptocurrencyaccountidmd) | ✅ | ✅ | ✅
| [`BytecodeFileId`](#bytecodefileid-fileidreferencefilefileidmd) | ✅ | ✅ | ✅
</details>

> class `ContractUpdateTransaction` extends [`Transaction`](reference/Transaction.md)

<!-- tabs:start -->

#### ** Java **

```java
new ContractUpdateTransaction()
    .setContractId(contractId)
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .setContractMemo("[e2e::ContractUpdateTransaction]")
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await new ContractUpdateTransaction()
        .setContractId(contract)
        .setNodeAccountIds([response.nodeId])
        .setContractMemo("[e2e::ContractUpdateTransaction]")
        .setMaxTransactionFee(new Hbar(5))
        .execute(client)
).getReceipt(client);
```

#### ** Go **

```go
response, err := hedera.NewContractUpdateTransaction().
    SetContractID(contractID).
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetContractMemo("[e2e::ContractUpdateTransaction]").
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

### Properties

##### `ContractId`: [`ContractId`](reference/contract/ContractId.md)

---

##### `AdminKey`: [`Key`](reference/cryptography/Key.md)

---

##### `ExpirationTime`: `Instant`

---

##### `ProxyAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

---

##### `AutoRenewPeriod`: `Duration`

---

##### `BytecodeFileId`: [`FileId`](reference/file/FileId.md)

---

##### `ContractMemo`: `String`

---
