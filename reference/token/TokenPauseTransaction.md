> class `TokenPauseTransaction` extends [`Transaction`](reference/core/Transaction.md)

Pauses the Token from being involved in any kind of Transaction until it is unpaused. Must be signed
with the Token's pause key. If the provided token is not found, the transaction will resolve to
INVALID\_TOKEN\_ID. If the provided token has been deleted, the transaction will resolve to
TOKEN\_WAS\_DELETED. If no Pause Key is defined, the transaction will resolve to
TOKEN\_HAS\_NO\_PAUSE\_KEY. Once executed the Token is marked as paused and will be not able to be a
part of any transaction. The operation is idempotent - becomes a no-op if the Token is already
Paused.

<!-- tabs:start -->

#### ** Java **

```java
var receipt = new TokenPauseTransaction()
    .setTokenId(tokenId)
    .execute(client) // TransactionResponse
    .getReceipt(client); // TransactionReceipt
```

#### ** JavaScript **

```javascript
const transaction = new TokenPauseTransaction()
    .setTokenId(tokenId);

const response = await transaction.execute(client) // TransactionResponse;
const receipt = await response.getReceipt(client) // TransactionReceipt;
```

- `Duration` is `number` and is the number of seconds

#### ** Go **

```go
response, err := hedera.NewTokenPauseTransaction().
    SetTokenID(tokenID).
    Execute(client) // TransactionResponse
if err != nil {
    println(err.Error())
}

receipt, err := response.GetReceipt(client)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Constructor

##### `constructor`()

---

### Properties

##### `tokenId`: [`TokenId`](reference/TokenId.md)

The token to be paused.

---
