# class `ContractByteCodeQuery`

Retrieve the latest state of a bytecode.


Returns [`ContractByteCode`](./ContractByteCode.md) from [`execute`](../Query.md).

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

## Properties

### `ContractId` : [`ContractId`](reference/contract/ContractId.md)

The Contract for which information is being requested.

## Declaration

```typescript
class ContractByteCodeQuery extends Query<ContractByteCode> {
    constructor();

    getContractId(): ContractId;
    setContractId(ContractId: ContractId): this;
}
```
