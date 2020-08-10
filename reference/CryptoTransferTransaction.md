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
| [`constructor()`](#new) | ✅ | ✅ | ✅
| [`addRecipient()`](#addRecipient) | ✅ | ✅ | ✅
| [`addSender()`](#addSender) | ✅ | ✅ | ✅
| [`addTransfer()`](#addTransfer) | ✅ | ✅ | ✅

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

#### Parameters

##### `id`

The Account ID of the sending party.

##### `amount`

The amount of `Hbar` that will be withdrawn/deposited from/to this account
for the transfer.

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
