# `TokenDissociateTransaction`

> class `TokenDissociateTransaction` extends [`Transaction`](reference/Transaction.md)

Dissociates the provided account with the provided tokens. Must be signed by the provided Account's key.

If the provided account is not found, the transaction will resolve to
[`Status.INVALID_ACCOUNT_ID`](reference/Status.md#INVALID_ACCOUNT_ID).

If the provided account has been deleted, the transaction will resolve to
[`Status.ACCOUNT_DELETED`](reference/Status.md#ACCOUNT_DELETED).

If any of the provided tokens is not found, the transaction will resolve to
[`Status.INVALID_TOKEN_REF`](reference/Status.md#INVALID_TOKEN_REF).

If any of the provided tokens has been deleted, the transaction will resolve to
[`Status.TOKEN_WAS_DELETED`](reference/Status.md#TOKEN_WAS_DELETED).

If an association between the provided account and any of the tokens does not exist, the transaction will resolve to
[`Status.TOKEN_NOT_ASSOCIATED_TO_ACCOUNT`](reference/Status.md#TOKEN_NOT_ASSOCIATED_TO_ACCOUNT).

If the provided account has a nonzero balance with any of the provided tokens, the transaction will resolve to
[`Status.TRANSACTION_REQUIRES_ZERO_TOKEN_BALANCES`](reference/Status.md#TRANSACTION_REQUIRES_ZERO_TOKEN_BALANCES).

On success, associations between the provided account and tokens are removed.

<!-- tabs:start -->

#### ** Java **

```java
newTokenId = new TokenDissociateTransaction()
    .setTokenId(new TokenId(4))
    .setAccountId(new AccountId(3))
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await (
        await new TokenDissociateTransaction()
            .setTokenIds([token])
            .setAccountId(account)
            .freezeWith(client)
            .sign(key)
    ).execute(client)
).getReceipt(client);
```

#### ** Go **

```go
dissociateTx, err := hedera.NewTokenDissociateTransaction().
    SetNodeAccountIDs([]AccountID{response.NodeID}).
    SetAccountID(accountID).
    SetTokenIDs(tokenID).
    FreezeWith(client)
if err != nil {
    println(err.Error())
}

response, err = dissociateTx.
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

### Properties

##### `tokenIds`: [`TokenId[]`](reference/token/TokenId.md)

The tokens to be dissociated with the provided account

---

##### `accountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The account to be dissociated with the provided tokens

---
