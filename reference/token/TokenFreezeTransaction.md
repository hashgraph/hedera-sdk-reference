# `TokenFreezeTransaction`

> class `TokenFreezeTransaction` extends [`Transaction`](reference/Transaction.md)

Freezes transfers of the specified token for the account. Must be signed by the Token's freezeKey.

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

If Freeze Key is not present in the Token, transaction results in TOKEN_HAS_NO_Freeze_KEY.
[`Status.TOKEN_HAS_NO_FREEZE_KEY`](reference/Status.md#TOKEN_HAS_NO_FREEZE_KEY).

Once executed the Account is marked as Frozen and will not be able to receive or send tokens unless unfrozen.
The operation is idempotent.

<!-- tabs:start -->

#### ** Java **

```java
newTokenId = new TokenFreezeTransaction()
    .setTokenId(new TokenId(4))
    .setAccountId(new AccountId(3))
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
// TODO
```

#### ** Go **

```go
// TODO
```

<!-- tabs:end -->

### Properties

##### `tokenId`: [`TokenId`](reference/token/TokenId.md)

The token for which this account will be frozen. If token does not exist, transaction results in
[`Status.INVALID_TOKEN_ID`](reference/Status.md#INVALID_TOKEN_ID).

---

##### `accountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The account to be frozen

---
