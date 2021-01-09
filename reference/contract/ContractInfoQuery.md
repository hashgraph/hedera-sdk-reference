# class `ContractInfoQuery`

Retrieve the latest state of a contract.

Returns [`ContractInfo`](./ContractInfo.md) from [`execute`](../Query.md).

## Static Methods

### `constructor()`

Creates an empty transaction, ready for configuration.

## Properties

### `ContractId` : [`ContractId`](reference/contract/ContractId.md)

The Contract for which information is being requested.

## Declaration

```typescript
class ContractInfoQuery extends Query<ContractInfo> {
    constructor();

    getContractId(): ContractId;
    setContractId(ContractId: ContractId): this;
}
```
