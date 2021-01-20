# `TokenRevokeKycTransaction`

> class `TokenRevokeKycTransaction` extends [`Transaction`](reference/core/Transaction.md)

Revokes KYC to the account for the given token. Must be signed by the Token's kycKey.

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

If RevokeKyc Key is not present in the Token, transaction results in TOKEN_HAS_NO_RevokeKyc_KEY.
[`Status.TOKEN_HAS_NO_KYC_KEY`](reference/Status.md#TOKEN_HAS_NO_KYC_KEY).

Once executed the Account is marked as KYC Revoked

<!-- tabs:start -->

#### ** Java **

```java
newTokenId = new TokenRevokeKycTransaction()
    .setTokenId(new TokenId(4))
    .setAccountId(new AccountId(3))
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await (
        await new TokenRevokeKycTransaction()
            .setTokenId(token)
            .setAccountId(account)
            .freezeWith(client)
            .sign(key)
    ).execute(client)
).getReceipt(client);
```

#### ** Go **

```go
response, err = hedera.NewTokenRevokeKycTransaction().
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

### Constructor

##### `constructor`()

---

### Properties

##### `tokenId`: [`TokenId`](reference/token/TokenId.md)

The token for which this account will get his KYC revoked. If token does not exist, transaction results in
[`Status.INVALID_TOKEN_ID`](reference/Status.md#INVALID_TOKEN_ID).

---

##### `accountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The account to be KYC Revoked

---
