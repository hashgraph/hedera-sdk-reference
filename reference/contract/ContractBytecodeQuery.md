# class `ContractByteCodeQuery`

Retrieve the latest state of a bytecode.


Returns [`ContractByteCode`](./ContractByteCode.md) from [`execute`](../Query.md).

## Static Methods

### `constructor()`

Creates an empty transaction, ready for configuration.

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
