# `ContractDeleteTransaction`

<details>
<summary><b>Support</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`ContractId`](#contractid-contractidreferencecontractcontractidmd) | ✅ | ✅ | ✅
| [`TransferAccountId`](#transferaccountid-accointidreferencecryptocurrencyaccountidmd) | ✅ | ✅ | ✅
| [`TransferContractId`](#transfercontractid-contractidreferencecontractcontractidmd) | ✅ | ✅ | ✅
</details>

> class `ContractDeleteTransaction` extends [`Transaction`](reference/Transaction.md)

<!-- tabs:start -->

#### ** Java **

```java
new ContractDeleteTransaction()
    .setContractId(contractId)
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await new ContractDeleteTransaction()
        .setContractId(contract)
        .setNodeAccountIds([response.nodeId])
        .execute(client)
).getReceipt(client);
```

#### ** Go **

```go
response, err := NewContractDeleteTransaction().
    SetContractID(contractID).
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
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

##### `TransferAccountId`: [`AccointId`](reference/cryptocurrency/AccountId.md)

---

##### `TransferContractId`: [`ContractId`](reference/contract/ContractId.md)

---
