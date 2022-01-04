# Transaction ID Generation

### Why

When submitting transactions especially chunked transactions sometimes the request fails with `TRANSACTION_EXPIRED`. We
should strive to prevent such an issue from being reported to the user and instead handle it from within the SDK.

### How

Whenever we receive a `TRANSACTION_EXPIRED` status and the user did not manually set the transaction IDs, we should
generate a new transaction ID per chunk.

- Generate new transaction IDs
- Clear `outerTransactions` list
- Clear `innerSignedTransactions` list

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
and clear **the chunks** `innerSignedTransactions` and
`outerTransactions`.
