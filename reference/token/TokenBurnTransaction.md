# `TokenBurnTransaction`

> class `TokenBurnTransaction` extends [`Transaction`](reference/Transaction.md)

Burns tokens from the Token's treasury Account. If no Supply Key is defined, the transaction will resolve to
[`Status.TOKEN_HAS_NO_SUPPLY_KEY`](reference/Status.md#TOKEN_HAS_NO_SUPPLY_KEY).
The operation decreases the Total Supply of the Token. Total supply cannot go below zero.
The amount provided must be in the lowest denomination possible. Example:
Token A has 2 decimals. In order to burn 100 tokens, one must provide amount of 10000. In order to burn 100.55 tokens,
one must provide amount of 10055.

<!-- tabs:start -->

#### ** Java **

```java
newTokenID = new TokenBurnTransaction()
    .setTokenId(new TokenId(4))
    .setAmount(10)
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
response = await new TokenBurnTransaction()
    .setAmount(10)
    .setTokenId(tokenId)
    .execute(client)

newTokenID = (await response.getReceipt(client)).tokenId;
```

#### ** Go **

```go
resp, err = NewTokenBurnTransaction().
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetAmount(10).
    SetTokenID(tokenID).
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

##### `tokenId`: [`TokenId`](reference/token/TokenId.md)

The token for which to burn tokens. If token does not exist, transaction results in
[`Status.INVALID_TOKEN_ID`](reference/Status.md#INVALID_TOKEN_ID).

---

##### `amount`: `Uint64`

The amount to burn from the Treasury Account. Amount must be a positive non-zero number, not bigger than the token
balance of the treasury account (0; balance], represented in the lowest denomination.

---
