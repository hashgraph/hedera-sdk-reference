# `TokenUnfreezeTransaction`

> class `TokenUnfreezeTransaction` extends [`Transaction`](reference/Transaction.md)

Unfreezes transfers of the specified token for the account. Must be signed by the Token's freezeKey.

If the provided account is not found, the transaction will resolve to
[`Status.INVALID_ACCOUNT_ID`](reference/Status.md#INVALID_ACCOUNT_ID).

If the provided account has been deleted, the transaction will resolve to
[`Status.ACCOUNT_DELETED`](reference/Status.md#ACCOUNT_DELETED).

If the provided token is not found, the transaction will resolve to
[`Status.INVALID_TOKEN_ID`](reference/Status.md#INVALID_TOKEN_ID).

If the provided token has been deleted, the transaction will resolve to
[`Status.TOKEN_WAS_DELETED`](reference/Status.md#TOKEN_WAS_DELETED).

If an Association between the provided token and account is not found, the transaction will resolve to
[`Status.TOKEN_NOT_ASSOCIATED_TO_ACCOUNT`](reference/Status.md#TOKEN_NOT_ASSOCIATED_TO_ACCOUNT).

If Unfreeze Key is not present in the Token, transaction results in TOKEN_HAS_NO_Unfreeze_KEY.
[`Status.TOKEN_HAS_NO_UNFREEZE_KEY`](reference/Status.md#TOKEN_HAS_NO_UNFREEZE_KEY).

Once executed the Account is marked as Unfrozen and will be able to receive or send tokens. The operation is idempotent.

<!-- tabs:start -->

#### ** Java **

```java
newTokenId = new TokenUnfreezeTransaction()
    .setTokenId(new TokenId(4))
    .setAccountId(new AccountId(3))
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await (
        await new TokenFreezeTransaction()
            .setTokenId(token)
            .setAccountId(account)
            .freezeWith(client)
            .sign(key)
    ).execute(client)
).getReceipt(client);
```

#### ** Go **

```go
response, err = NewTokenFreezeTransaction().
    SetNodeAccountIDs([]AccountID{response.NodeID}).
    SetAccountID(accountID).
    SetTokenID(tokenID).
    Execute(client)
if err != nil {
    println(err.Error())
}

_, err = response.GetReceipt(client)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Properties

##### `tokenId`: [`TokenId`](reference/token/TokenId.md)

The token for which this account will be unfrozen. If token does not exist, transaction results in
[`Status.INVALID_TOKEN_ID`](reference/Status.md#INVALID_TOKEN_ID).

---

##### `accountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The account to be unfrozen

---
