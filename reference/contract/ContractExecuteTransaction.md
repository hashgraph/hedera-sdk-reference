# `ContractExecuteTransaction`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`ContractId`](#contractid-contractidreferencecontractcontractidmd) | ✅ | ✅ | ✅
| [`Gas`](#gas-uint64) | ✅ | ✅ | ✅
| [`PayableAmount`](#payableamount-hbarreferencehbarmd) | ✅ | ✅ | ✅
| [`FunctionParameters`](#functionparameters-bytestring) | ✅ | ✅ | ✅
| [`Function`](#write-only-function-this) | ✅ | ✅ | ✅
</details>

> class `ContractExecuteTransaction` extends [`Transaction`](reference/Transaction.md)

<!-- tabs:start -->

#### ** Java **

```java
new ContractExecuteTransaction()
    .setContractId(contractId)
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .setGas(10000)
    .setFunction("setMessage", new ContractFunctionParameters().addString("new message"))
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await new ContractExecuteTransaction()
        .setContractId(contract)
        .setNodeAccountIds([response.nodeId])
        .setGas(10000)
        .setFunction(
            "setMessage",
            new ContractFunctionParameters().addString("new message")
        )
        .setMaxTransactionFee(new Hbar(5))
        .execute(client)
).getReceipt(client);
```

#### ** Go **

```go
response, err := hedera.NewContractExecuteTransaction().
    SetContractID(contractID).
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetGas(10000).
    SetFunction("setMessage", NewContractFunctionParameters().AddString("new message")).
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

##### `Gas`: `Uint64`

---

##### `PayableAmount`: [`Hbar`](reference/Hbar.md)

---

##### `FunctionParameters`: `bytes`

---

##### **Write-only** `Function`: `this`

---
