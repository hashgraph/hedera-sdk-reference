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
const newKey = PrivateKey.generate();

const accountCreateTransaction = new AccountCreateTransaction({
    key: newKey,
    initialBalance: new Hbar(10),
});

const response = await accountCreateTransaction.execute(client);
const receipt = await response.getReceipt(client);

const newAccountId = receipt.accountId;
```

- `Duration` is `number` and is the number of seconds

#### ** Go **

```go
newKey := hedera.GeneratePrivateKey()

response, err := NewAccountCreateTransaction().
    SetKey(newKey).
    SetInitialBalance(10 * hedera.Hbar) // 10 Hbars
    Execute(client) // TransactionResponse
if err != nil {
    println(err.Error())
}

receipt, err := response.GetReceipt(client)
if err != nil {
    println(err.Error())
}

accountID := *receipt.AccountID
```

<!-- tabs:end -->

### Properties

##### `AccountId`: [`AccountId`](reference/cryptography/AccountId.md)

---
##### `TransferAccountId`: [`AccountId`](reference/cryptography/AccountId.md)

---

