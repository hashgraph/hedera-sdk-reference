# `TokenMintTransaction`

> class `TokenMintTransaction` extends [`Transaction`](reference/Transaction.md)

Mints tokens to the Token's treasury Account. If no Supply Key is defined, the transaction will resolve to
[`Status.TOKEN_HAS_NO_SUPPLY_KEY`](reference/Status.md#TOKEN_HAS_NO_SUPPLY_KEY).
The operation increases the Total Supply of the Token. The maximum total supply a token can have is 2^63-1.
The amount provided must be in the lowest denomination possible. Example:
Token A has 2 decimals. In order to mint 100 tokens, one must provide amount of 10000. In order to mint 100.55 tokens,
one must provide amount of 10055.

<!-- tabs:start -->

#### ** Java **

```java
newTokenId = new TokenMintTransaction()
    .setTokenId(new TokenId(4))
    .setAmount(10)
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await new TokenMintTransaction()
        .setAmount(10)
        .setTokenId(tokenId)
        .execute(client)
).getReceipt(client);
```

#### ** Go **

```go
resp, err = NewTokenMintTransaction().
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

The token for which to mint tokens. If token does not exist, transaction results in
[`Status.INVALID_TOKEN_ID`](reference/Status.md#INVALID_TOKEN_ID).

---

##### `amount`: `Uint64`

The amount to mint to the Treasury Account. Amount must be a positive non-zero number represented in the lowest
denomination of the token. The new supply must be lower than 2^63.on.

---
