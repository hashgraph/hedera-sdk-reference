# `TokenTransferTransaction`

> class `TokenTransferTransaction` extends [`Transaction`](reference/Transaction.md)

Transfer tokens from some accounts to other accounts. Each negative amount is withdrawn from the corresponding account
(a sender), and each positive one is added to the corresponding account (a receiver). All amounts must have sum of zero.
Each amount is a number with the lowest denomination possible for a token. Example:
Token X has 2 decimals. Account A transfers amount of 100 tokens by providing 10000 as amount in the TransferList.
If Account A wants to send 100.55 tokens, he must provide 10055 as amount.

If any sender account fails to have sufficient token balance, then the entire transaction fails and none of the
transfers occur, though transaction fee is still charged.

<!-- tabs:start -->

#### ** Java **

```java
newTokenId = new TokenTransferTransaction()
    .addSender(new TokenId(4), new AccountId(3), 10)
    .addRecipient(new TokenId(4), new AccountId(5), 10)
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await new TransferTransaction()
        .addTokenTransfer(token, account, 10)
        .addTokenTransfer(token, client.operatorAccountId, -10)
        .execute(client)
).getReceipt(client);
```

#### ** Go **

```go
resp, err = NewTransferTransaction().
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

### Properties

##### `transfers`: `Map<`[`TokenId`](reference/token/TokenId.md), [`TokenTransfer[]`](reference/token/TokenTransfer.md)`>`

The transfers for each token.

If any of the token tokens do not exist, transaction results in
[`Status.INVALID_TOKEN_ID`](reference/Status.md#INVALID_TOKEN_ID).

If the sum of the transfers per token is not 0, transaction results in
[`Status.TRANSFERS_NOT_ZERO_SUM_FOR_TOKEN`](reference/Status.md#TRANSFERS_NOT_ZERO_SUM_FOR_TOKEN).

---
