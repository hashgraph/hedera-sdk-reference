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

### Methods

##### `setFunction` ( `name`: `String` ): `ContractCallQuery`

---

##### `setFunction` ( `name`: `String`, `params`: `ContractFunctionParameters` ): `ContractCallQuery`

---

`Function`: `ContractCallQuery`

## Properties

##### `contractId`: [`ContractId`](reference/contract/ContractId.md)

The `ContractId` for which information is being requested.

---

##### `gas`: `Uint64`

The amount of gas to use for the call.
All of the gas offered will be used and charged a corresponding fee.

---

##### `functionParameters`: `bytes`

Which function to call, and the parameters to pass to the function

---

##### **Write-only** `MaxResultSize`: `ContractCallQuery`

Maximum number of bytes that the result might include. The run will fail if it is returning more than this number of bytes.

---
