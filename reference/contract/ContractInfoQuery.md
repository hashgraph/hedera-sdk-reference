> class `ContractInfoQuery` extends [`Query`](reference/core/Query.md) < [`ContractInfo`](reference/contract/ContractInfo.md) >

Retrieve the latest state of a contract.

<!-- tabs:start -->

#### ** Java **

```java
var info = new ContractInfoQuery()
    .setContractId(contractId)
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .execute(client);
```

#### ** JavaScript **

```javascript
let info = await new ContractInfoQuery()
    .setNodeAccountIds([response.nodeId])
    .setContractId(contract)
    .setQueryPayment(new Hbar(1))
    .execute(client);
```

#### ** Go **

```go
info, err := hedera.NewContractInfoQuery().
    SetContractID(contractID).
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetMaxQueryPayment(NewHbar(2)).
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

This is the contractc ID for which info will be queried for.

---
