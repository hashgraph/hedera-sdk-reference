> class `ContractByteCodeQuery` extends [`Query`](reference/core/Query.md) < `bytes` >

Retrieve the latest state of a bytecode.

<!-- tabs:start -->

#### ** Java **

```java
var bytecode = new ContractByteCodeQuery()
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .setContractId(contractId)
    .execute(client);
```

#### ** JavaScript **

```javascript
const bytecode = await new ContractByteCodeQuery()
    .setNodeAccountIds([response.nodeId])
    .setContractId(contract)
    .setQueryPayment(new Hbar(2))
    .execute(client);
```

#### ** Go **

```go
bytecode, err := hedera.NewContractBytecodeQuery().
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetContractID(contractID).
    SetQueryPayment(NewHbar(2)).
    Execute(client)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Constructor

##### `constructor`()

---

## Properties

### `contractId` : [`ContractId`](reference/contract/ContractId.md)

This is the contract ID which bytecode will be queried for.

---
