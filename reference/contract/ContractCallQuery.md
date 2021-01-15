# class `ContractCallQuery`

Retrieve the latest state of a contract call.


Returns [`ContractCall`](./ContractCall.md) from [`execute`](../Query.md).

<details>
<summary><b>Declaration</b></summary>

```typescript
class ContractCallQuery extends Query<ContractCall> {
    constructor();

    /* property */ contractId
    /* property */ gas
    /* property */ functionParameters
    /* property */ maxResultSize
}
```

</details>

<!-- tabs:start -->

#### ** Java **

```java
var callQuery = new ContractCallQuery()
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .setContractId(contractId)
    .setGas(2000)
    .setFunction("getMessage");

    var cost = callQuery.getCost(client);

var result = callQuery
    .setMaxQueryPayment(Objects.requireNonNull(cost))
    .execute(client);
```

#### ** JavaScript **

```javascript
const callQuery = new ContractCallQuery()
    .setNodeAccountIds([response.nodeId])
    .setContractId(contract)
    .setQueryPayment(new Hbar(1))
    .setGas(2000)
    .setFunction("getMessage");

const cost = callQuery.getCost(client);

let result = await callQuery
    .setMaxQueryPayment(cost)
    .execute(client);
```

#### ** Go **

```go
result, err := hedera.NewContractCallQuery().
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetContractID(contractID).
    SetQueryPayment(NewHbar(1)).
    SetGas(2000).
    SetFunction("getMessage", nil).
    SetMaxQueryPayment(NewHbar(5)).
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

##### `contractId`: [`ContractId`](reference/contract/ContractId.md)

The Contract for which information is being requested.

---

##### `Gas`: `Uint64`

---

##### `FunctionParameters`: `bytes`

---

##### **Write-only** `Function`: `ContractCallQuery`

---

##### **Write-only** `MaxResultSize`: `ContractCallQuery`

---
