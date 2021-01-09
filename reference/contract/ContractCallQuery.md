# class `ContractCallQuery`

Retrieve the latest state of a contract call.


Returns [`ContractCall`](./ContractCall.md) from [`execute`](../Query.md).

## Static Methods

### `constructor()`

Creates an empty transaction, ready for configuration.

## Properties

##### `ContractId`: [`ContractId`](reference/contract/ContractId.md)

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

## Declaration

```typescript
class ContractCallQuery extends Query<ContractCall> {
    constructor();

    getContractId(): ContractId;
    setContractId(ContractId: ContractId): this;
}
```
