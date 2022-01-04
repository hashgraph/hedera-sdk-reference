# Transaction ID Generation

### Why

When submitting transactions especially chunked transactions sometimes the request fails with `TRANSACTION_EXPIRED`. We
should strive to prevent such an issue from being reported to the user and instead handle it from within the SDK.

### How to lock transaction IDs

```javascript
class LockedList {
    constructor() {
        this.list = [];
        this.index = 0;
        this.locked = false;
    }
}
```

### Methods that should freeze transaction ID list

- `Transaction.fromBytes()`
- `Transaction.getTransactionHash()`
- `Transaction.getTransactionHashPerNode()`
- `Transaction.toBytes()`
- `Transaction.addSignature()`
- `Transaction.getTransactionId()`
- `Transaction.setTransactionId()`
- `Transaction.getSignatures()`

### Execute behavior

When a transaction fails with `TRANSACTION_EXPIRED` we should generate a new transaction ID for that particular chunk
and clear **the chunks** `signedTransactions` and
`transactions`.
