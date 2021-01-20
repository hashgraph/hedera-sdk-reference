# `ContractDeleteTransaction`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`ContractId`](#contractid-contractidreferencecontractcontractidmd) | ✅ | ✅ | ✅
| [`TransferAccountId`](#transferaccountid-accointidreferencecryptocurrencyaccountidmd) | ✅ | ✅ | ✅
| [`TransferContractId`](#transfercontractid-contractidreferencecontractcontractidmd) | ✅ | ✅ | ✅
</details>

> class `ContractDeleteTransaction` extends [`Transaction`](reference/core/Transaction.md)

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

The `ContractId` of the contract to be deleted.

---

##### `transferAccountId`: [`AccointId`](reference/cryptocurrency/AccountId.md)

The `AccountId` of an account to receive any remaining `Hbar` from the deleted contract.

---

##### `transferContractId`: [`ContractId`](reference/contract/ContractId.md)

The `ContractId` of a contract to receive any remaining `Hbar` from the deleted contract

---
