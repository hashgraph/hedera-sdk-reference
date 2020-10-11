# `CryptoTransferTransaction`

> class `CryptoTransferTransaction` extends [`Transaction`](reference/core/Transaction.md)

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

<!-- tabs:start -->

### ** Java **

```java
// transfer 10 ħ from sender to recipient
new CryptoTransferTransaction()
    .addSender(senderId, new Hbar(10))
    .addRecipient(recipientId, new Hbar(10))
    .execute(client);
```

### ** JavaScript **

```javascript
// transfer 10 ħ from sender to recipient
await new CryptoTransferTransaction({ transfers: [
    { accountId: senderId, amount: 10 },
    { accountId: recipientId, amount: -10 },
]}).execute(client);
```

### ** Go **

```go
// transfer 10 ħ from sender to recipient
_, err := NewCryptoTransferTransaction().
    AddSender(senderID, NewHbar(10)).
    AddReceipient(recipientID, NewHbar(10)).
    Execute(client)
```

<!-- tabs:end -->

### Constructor

##### `constructor` ()

---

### Methods

##### `addSender` ( `id`: `AccountId`, `amount`: `Hbar` ): `this`

Add a party to the transfer who will have currency withdrawn from their account
to add to the transfer.

---

##### `addRecipient` ( `id`: `AccountId`, `amount`: `Hbar` ): `this`

Add a party to the transfer who will have currency credited to their account
by this transfer.

---

##### `addTransfer` ( `id`: `AccountId`, `amount`: `Hbar` ): `this`

---

### Properties

##### `transfers`: `Transfer[]`

---
