> class `TokenAssociateTransaction` extends [`Transaction`](reference/core/Transaction.md)

Associates the provided account with the provided tokens. Must be signed by the provided Account's key.

If the provided account is not found, the transaction will resolve to
[`Status.INVALID_ACCOUNT_ID`](reference/Status.md#INVALID_ACCOUNT_ID).

If the provided account has been deleted, the transaction will resolve to
[`Status.ACCOUNT_DELETED`](reference/Status.md#ACCOUNT_DELETED).

If any of the provided tokens is not found, the transaction will resolve to
[`Status.INVALID_TOKEN_REF`](reference/Status.md#INVALID_TOKEN_REF).

If any of the provided tokens has been deleted, the transaction will resolve to
[`Status.TOKEN_WAS_DELETED`](reference/Status.md#TOKEN_WAS_DELETED).

If an association between the provided account and any of the tokens already exists, the transaction will resolve to
[`Status.TOKEN_ALREADY_ASSOCIATED_TO_ACCOUNT`](reference/Status.md#TOKEN_ALREADY_ASSOCIATED_TO_ACCOUNT).

If the provided account's associations count exceed the constraint of maximum token associations per account, the
transaction will resolve to
[`Status.TOKENS_PER_ACCOUNT_LIMIT_EXCEEDED`](reference/Status.md#TOKENS_PER_ACCOUNT_LIMIT_EXCEEDED).

On success, associations between the provided account and tokens are made and the account is ready to interact with
the tokens.

<!-- tabs:start -->

#### ** Java **

```java
newTokenId = new TokenAssociateTransaction()
    .setTokenId(new TokenId(4))
    .setAccountId(new AccountId(3))
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await (
        await new TokenAssociateTransaction()
            .setTokenIds([token])
            .setAccountId(account)
            .freezeWith(client)
            .sign(key)
    ).execute(client)
).getReceipt(client);
```

#### ** Go **

```go
transaction, err := hedera.NewTokenAssociateTransaction().
    SetNodeAccountIDs([]AccountID{response.NodeID}).
    SetAccountID(accountID).
    SetTokenIDs(tokenID).
    FreezeWith(client)
if err != nil {
    println(err.Error())
}

response, err = transaction.
    Sign(newKey).
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

### Constructor

##### `constructor`()

---

### Properties

##### `tokenIds`: [`TokenId[]`](reference/token/TokenId.md)

The tokens to be associated with the provided account

---

##### `accountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The account to be associated with the provided tokens

---
