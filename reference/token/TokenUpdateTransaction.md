# `TokenUpdateTransaction`

> class `TokenUpdateTransaction` extends [`Transaction`](reference/core/Transaction.md)

Updates an already created Token.

If no value is given for a field, that field is left unchanged. For an immutable tokens (that is, a token created
without an adminKey), only the expiry may be updated. Setting any other field in that case will cause the transaction
status to resolve to
[`Status.TOKEN_IS_IMMUTABlE`](reference/Status.md#TOKEN_IS_IMMUTABlE).

<!-- tabs:start -->

#### ** Java **

```java
newTokenId = new TokenUpdateTransaction()
    .setTokenId(new TokenId(4))
    .setName("ffff")
    .setSymbol("F")
    .setTreasury(OPERATOR_ID)
    .setAdminKey(OPERATOR_KEY.publicKey)
    .setFreezeKey(OPERATOR_KEY.publicKey)
    .setWipeKey(OPERATOR_KEY.publicKey)
    .setKycKey(OPERATOR_KEY.publicKey)
    .setSupplyKey(OPERATOR_KEY.publicKey)
    .execute(client)
    .getReceipt(client)
    .tokenId;
```

#### ** JavaScript **

```js
await (
    await new TokenUpdateTransaction()
        .setNodeAccountIds([response.nodeId])
        .setTokenId(token)
        .setTokenName("aaaa")
        .setTokenSymbol("A")
        .execute(client)
).getReceipt(client);
```

- `Duration` is `number` and is the number of seconds

#### ** Go **

```go
response, err = hedera.NewTokenUpdateTransaction().
    SetTokenID(tokenID).
    SetTokenSymbol("A").
    SetNodeAccountIDs([]AccountID{response.NodeID}).
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

##### `tokenId`: `TokenId`

The Token to be updated

---

##### `name`: `String`

The new Name of the Token. Must be a string of ASCII characters.

---

##### `symbol`: `String`

The new Symbol of the Token. Must be UTF-8 capitalized alphabetical string identifying the token.

---

##### `treasuryAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The new Treasury account of the Token. If the provided treasury account is not existing or deleted, the response will be
[`Status.INVALID_TREASURY_ACCOUNT_FOR_TOKEN`](reference/Status.md#INVALID_TREASURY_ACCOUNT_FOR_TOKEN).
If successful, the Token balance held in the previous Treasury Account is
transferred to the new one.

---

##### `adminKey`: [`Key`](reference/cryptography/Key.md)

The new Admin key of the Token. If Token is immutable, transaction will resolve to
[`Status.TOKEN_IS_IMMUTABlE`](reference/Status.md#TOKEN_IS_IMMUTABlE).

---

##### `kycKey`: [`Key`](reference/cryptography/Key.md)

The new KYC key of the Token. If Token does not have currently a KYC key, transaction will resolve to
[`Status.TOKEN_HAS_NO_KYC_KEY`](reference/Status.md#TOKEN_HAS_NO_KYC_KEY).

---

##### `freezeKey`: [`Key`](reference/cryptography/Key.md)

The new Freeze key of the Token. If the Token does not have currently a Freeze key, transaction will resolve to
[`Status.TOKEN_HAS_NO_FREEZE_KEY`](reference/Status.md#TOKEN_HAS_NO_FREEZE_KEY).


---

##### `wipeKey`: [`Key`](reference/cryptography/Key.md)

The new Wipe key of the Token. If the Token does not have currently a Wipe key, transaction will resolve to
[`Status.TOKEN_HAS_NO_WIPE_KEY`](reference/Status.md#TOKEN_HAS_NO_WIPE_KEY).

---

##### `supplyKey`: [`Key`](reference/cryptography/Key.md)

The new Supply key of the Token. If the Token does not have currently a Supply key, transaction will resolve to
[`Status.TOKEN_HAS_NO_SUPPLY_KEY`](reference/Status.md#TOKEN_HAS_NO_SUPPLY_KEY).

---

##### `expirationTime`: [`Timestamp`](reference/Timestamp.md)

The new expiry time of the token. Expiry can be updated even if admin key is not set. If the provided expiry is earlier
than the current token expiry, transaction wil resolve to
[`Status.INVALID_EXPIRATION_TIME`](reference/Status.md#INVALID_EXPIRATION_TIME).


---

##### `autoRenewAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The new account which will be automatically charged to renew the token's expiration, at autoRenewPeriod interval.

---

##### `autoRenewPeriod`: [`Duration`](reference/Duration.md)

The new interval at which the auto-renew account will be charged to extend the token's expiry.

---
