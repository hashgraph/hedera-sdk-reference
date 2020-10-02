# `CryptoTransferTransaction`

Transfer cryptocurrency from some accounts to other accounts.

* The accounts list can contain up to 10 accounts.

* The amounts list must be the same length as the accounts list.

* Each negative amount is withdrawn from the corresponding account (a sender),
    and each positive one is added to the corresponding account (a receiver).

* The amounts list must sum to zero. Each amount is a number of tinyBars.

* If any sender account fails to have sufficient hbars to do the withdrawal,
    then the entire transaction fails, and none of those transfers occur,
    though the transaction fee is still charged.

* This transaction must be signed by the keys for all the
    sending accounts, and for any receiving accounts that
    have `receiverSignatureRequired` set to `true`.

## Support

| Item | Java | JavaScript | Go
| - |:-: |:-: |:-: |
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`addRecipient()`](#addrecipient) | ✅ | ✅ | ✅
| [`addSender()`](#addsender) | ✅ | ✅ | ✅
| [`addTransfer()`](#addtransfer) | ✅ | ✅ | ✅
| [`getTransfers()`](#gettransfers) | ✅ | ✅ | O
| [`execute()`](#execute) | ✅ | ✅ | O
| [`setNodeId()`](#setnodeid) | ✅ | ✅ | O
| [`getNodeId()`](#getnodeid) | ✅ | ✅ | O
| [`setTransactionValidDuration()`](#settransactionvalidduration) | ✅ | ✅ | O
| [`getTransactionValidDuration()`](#gettransactionvalidduration) | ✅ | ✅ | O
| [`setMaxTransactionFee()`](#setmaxtransactionfee) | ✅ | ✅ | O
| [`getMaxTransactionFee()`](#getmaxtransactionfee) | ✅ | ✅ | O
| [`setTransactionMemo()`](#settransactionmemo) | ✅ | ✅ | O
| [`getTransactionMemo()`](#gettransactionmemo) | ✅ | ✅ | O
| [`toBytes()`](#tobytes) | ✅ | ✅ | O
| [`fromBytes()`](#frombytes) | ✅ | ✅ | O
| [`getTransactionHash()`](#gettransactionhash) | ✅ | ✅ | O
| [`setTransactionId()`](#settransactionid) | ✅ | ✅ | O
| [`getTransactionId()`](#gettransactionid) | ✅ | ✅ | O
| [`sign()`](#sign) | ✅ | ✅ | O
| [`signWith()`](#signwith) | ✅ | ✅ | O
| [`signWithOperator()`](#signwithoperator) | ✅ | ✅ | O
| [`freeze()`](#freeze) | ✅ |  ✅ | O
| [`freezeWith()`](#freezewith) | ✅ | ✅ | O

## Methods

### `constructor()`

Creates a new `CryptoTransferTransaction` object.

```typescript
constructor()
```

### `addSender()`

Add a party to the transfer who will have currency withdrawn from their account
to add to the transfer.

```typescript
addSender(id: AccountId, amount: Hbar): this
```

Alias for:

```typescript
addTransfer(id, -amount)
```

### `addRecipient()`

Add a party to the transfer who will have currency credited to their account
by this transfer.

```typescript
addSender(id: AccountId, amount: Hbar): this
```

Alias for:

```typescript
addTransfer(id, amount)
```

### `addTransfer()`

```typescript
addTransfer(id: AccountId, amount: Hbar): this
```

### `getTransfers()`

```typescript
getTransfers(): List<Transfer>
```

### `execute()`

```typescript
async execute(client: Client): this
```

### `setNodeId()`

```typescript
setNodeId(id: AccountId): this
```

### `getNodeId()`

```typescript
getNodeId(): AccountId
```

### `setTransactionValidDuration()`

```typescript
setTransactionValidDuration(duration: Timestamp): this
```

### `getTransactionValidDuration()`

```typescript
getTransactionValidDuration(): Timestamp
```

### `setMaxTransactionFee()`

```typescript
setMaxTransactionFee(fee: Hbar): this
```

### `getMaxTransactionFee()`

```typescript
getMaxTransactionFee(): Hbar
```

### `setTransactionMemo()`

```typescript
setTransactionMemo(memo: string): this
```

### `getTransactionMemo()`

```typescript
getTransactionMemo(): string
```

### `toBytes()`

```typescript
toBytes(): bytes
```

### `fromBytes()`

```typescript
fromBytes(data: bytes): this
```

### `getTransactionHash()`

```typescript
getTransactionHash(): bytes
```

### `getTransactionId()`

```typescript
getTransactionId(): TransactionId
```

### `setTransactionId()`

```typescript
setTransactionId(id: TransactionId): this
```

### `sign()`

```typescript
sign(key: PrivateKey): this
```

### `signWith()`

```typescript
signWith(key: PublicKey, signer: Function<bytes, bytes>): this
```

### `signWithOperator()`

```typescript
signWithOperator(client: Client): this
```

### `freeze()`

```typescript
freeze(): this
```

### `freezeWith()`

```typescript
freezeWith(client: Client): this
```

## Examples

### Java

```java
var transactionId = new CryptoTransferTransaction()
    .addSender(senderId, new Hbar(10))
    // .addTransfer(senderId, new Hbar(-10))
    .addRecipient(recipientId, new Hbar(10))
    .execute(client);
```

### JavaScript

```javascript
let transactionId = await new CryptoTransferTransaction()
    .addSender(senderId, new Hbar(10))
    // .addTransfer(senderId, new Hbar(-10))
    .addRecipient(recipientId, new Hbar(10))
    .execute(client);
```

### Go

```go
transactionID, err:= NewCryptoTransferTransaction().
    AddSender(senderID, NewHbar(10)).
    // AddTransfer(senderId, NewHbar(-10)).
    AddReceipient(recipientID, NewHbar(10)).
    Execute(client)
```