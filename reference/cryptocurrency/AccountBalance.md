> class `AccountBalance`

Response when the client sends the node CryptoGetAccountBalanceQuery

<!-- tabs:start -->

#### ** Java **

```java
var balances = new AccountBalanceQuery()
    .setAccountId(operatorId)
    .execute(client);


System.out.println(balances.hbar); // Hbar balances
System.out.println(balances.tokens.get(new TokenId(3)); // Balance for token ID 3
System.out.println(balances.tokenDecimals.get(new TokenId(3)); // Token ID 3's decimal field
```

#### ** JavaScript **

```javascript
const balances = await new AccountBalanceQuery()
    .setAccountId("3") // balance of node 3
    .execute(client);

console.log(balances.hbar); // Hbar balances
console.log(balances.tokens.get(new TokenId(3)); // Balance for token ID 3
console.log(balances.tokenDecimals.get(new TokenId(3)); // Token ID 3's decimal field
```

#### ** Go **

```go
balances, err := hedera.NewAccountBalanceQuery().
    SetAccountID(client.GetOperatorAccountID()).
    Execute(client)
if err != nil {
    println(err.Error())
}

println(balances.Hbar); // Hbar balances
println(balances.Tokens.Get(TokenID{Token: 3}); // Balance for token ID 3
println(balances.TokenDecimals.get(TokenID{Token: 3}); // Token ID 3's decimal field
```

<!-- tabs:end -->

### Properties

##### `hbars`: [`Hbar`](/reference/Hbar.md)

The current balance, in tinybars.

---

##### `tokens`: `Map` < [`TokenId`](/reference/token/TokenId.md), `Uint64` >

The token balances possessed by the target account.

Number of transferable units of the identified token. For token of type FUNGIBLE\_COMMON -
balance in the smallest denomination. For token of type NON\_FUNGIBLE\_UNIQUE - the number of
NFTs held by the account

---

##### `tokenDecimals`: `Map` < [`TokenId`](/reference/token/TokenId.md), `Uint64` >

The token decimals for each token

Tokens divide into <tt>10<sup>decimals</sup></tt> pieces

---
