# class `ContractInfoQuery`

Retrieve the latest state of a contract.

Returns [`ContractInfo`](./ContractInfo.md) from [`execute`](../Query.md).

<details>
<summary><b>Declaration</b></summary>

```typescript
class ContractInfoQuery extends Query<ContractInfo> {
    constructor();

    getContractId(): ContractId;
    setContractId(ContractId: ContractId): this;
}
```

</details>

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

### `ContractId` : [`ContractId`](reference/contract/ContractId.md)

The Contract for which information is being requested.
