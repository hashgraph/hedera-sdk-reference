# `AccountDeleteTransaction`

> class `AccountDeletedTransaction` extends [`Transaction`](reference/Transaction.md)
> [!WARNING]
> When you delete an account, you need to sign it with the key set at account creation.


<!-- tabs:start -->

#### ** Java **

```java
new AccountDeleteTransaction()
    .setAccountId(accountId)
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .setTransferAccountId(operatorId)
    .freezeWith(client)
    .sign(key)
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await (
        await new AccountDeleteTransaction()
            .setAccountId(account)
            .setNodeAccountIds([response.nodeId])
            .setTransferAccountId(operatorId)
            .setTransactionId(TransactionId.generate(account))
            .freezeWith(client)
            .sign(key)
    ).execute(client)
).getReceipt(client);
```

- `Duration` is `number` and is the number of seconds

#### ** Go **

```go
newKey := hedera.GeneratePrivateKey()

transaction, err := hedera.NewAccountDeleteTransaction().
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetAccountID(accountID).
    SetTransferAccountID(client.GetOperatorAccountID()).
    SetTransactionID(TransactionIDGenerate(accountID)).
    FreezeWith(client)
if err != nil {
    println(err.Error())
}

resp, err = transaction.
    Sign(newKey).
    Execute(client)
if err != nil {
    println(err.Error())
}

_, err = resp.GetReceipt(client)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Properties

##### `AccountId`: [`AccountId`](reference/cryptography/AccountId.md)

---
##### `TransferAccountId`: [`AccountId`](reference/cryptography/AccountId.md)

---

