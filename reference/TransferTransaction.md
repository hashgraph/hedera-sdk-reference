# `TransferTransaction`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`tokenTransfers`](#tokentransfers-maptokenid-mapaccountid-long) | ✅ | ✅ | ✅
| [`hbarTransfers`](#hbartransfers-mapaccountid-hbar) | ✅ | ✅ | ✅

</details>

> class `TransferTransaction` extends [`Transaction`](reference/core/Transaction.md)

<!-- tabs:start -->

#### ** Java **

```java
receipt = new TransferTransaction()
    .addHbarTransfer(client.getOperatorAccountId(), Hbar.fromTinybars(-10))
    .addHbarTransfer(AccountId.fromString("0.0.3"), Hbar.fromTinybars(10))
    .execute(client)
    .getReceipt(client);

receipt = new TransferTransaction()
    .addTokenTransfer(tokenID, client.getOperatorAccountId(), -10)
    .addTokenTransfer(tokenID, AccountId.fromString("0.0.3"), 10)
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await new TransferTransaction()
        .addHbarTransfer(client.operatorAccountId, new Hbar(-10))
        .addHbarTransfer(new AccountId(3), new Hbar(10))
        .execute(client)
).getReceipt(client);

await (
    await new TransferTransaction()
        .addTokenTransfer(tokenID, client.operatorAccountId, -10)
        .addTokenTransfer(tokenID, new AccountId(3), 10)
        .execute(client)
).getReceipt(client);
```

#### ** Go **

```go
resp, err := hedera.NewTransferTransaction().
    AddHbarTransfer(client.GetOperatorAccountID(), NewHbar(-1)).
    AddHbarTransfer(AccountID{Account: 3}, NewHbar(1)).
    Execute(client)
if err != nil {
    println(err.Error())
}

_, err = resp.GetReceipt(client)
if err != nil {
    println(err.Error())
}

resp, err = hedera.NewTransferTransaction().
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    AddTokenTransfer(tokenID, client.GetOperatorAccountID(), -10).
    AddTokenTransfer(tokenID, accountID, 10).
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

### Constructor

##### `constructor`()

---

### Properties

##### `tokenTransfers`: `Map<TokenId, Map<AccountId, Long>>`

---

##### `hbarTransfers`: `Map<AccountId, Hbar>`

---

