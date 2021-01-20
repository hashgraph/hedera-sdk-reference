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

> class `ContractExecuteTransaction` extends [`Transaction`](reference/core/Transaction.md)

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

### Constructor

##### `constructor`()

---

### Methods

##### `setFunction` ( `name`: `String` ): `ContractExecuteTransaction`

---

##### `setFunction` ( `name`: `String`, `params`: `ContractFunctionParameters` ): `ContractExecuteTransaction`

---

### Properties

##### `contractId`: [`ContractId`](reference/contract/ContractId.md)

The `ContractId` if the instance to execute.

---

##### `gas`: `Uint64`

The maximum amount of gas to use for the execution.

---

##### `payableAmount`: [`Hbar`](reference/Hbar.md)

Number of tinybars sent.

---

##### `functionParameters`: `bytes`

Which function to execute, and the parameters to pass to the function.

---
