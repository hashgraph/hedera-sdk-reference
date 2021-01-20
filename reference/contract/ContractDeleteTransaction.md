> class `ContractDeleteTransaction` extends [`Transaction`](reference/core/Transaction.md)

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`contractId`](#contractid-contractid) | ✅ | ✅ | ✅
| [`transferAccountId`](#transferaccountid-accountid) | ✅ | ✅ | ✅
| [`transferContractId`](#transfercontractid-contractid) | ✅ | ✅ | ✅
</details>

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
response, err := hedera.NewContractDeleteTransaction().
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

### Constructor

##### `constructor`()

---

### Properties

##### `contractId`: [`ContractId`](reference/contract/ContractId.md)

The ID of the contract to be deleted.

---

##### `transferAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The ID of an account that will receive any remaining `Hbar` from the deleted contract.

---

##### `transferContractId`: [`ContractId`](reference/contract/ContractId.md)

The ID of a contract that will receive any remaining `Hbar` from the deleted contract

---
