> class `AccountAllowanceAdjustdTransaction` extends [`Transaction`](reference/core/Transaction.md)

 Modifies or creates the hbar/token allowance for a spender <b>relative to the payer account
 of this transaction</b>. 
 
 (So if account <tt>0.0.X</tt> pays for this transaction, then at consensus the spender 
 account will have new allowances to spend hbar or tokens from <tt>0.0.X</tt>). 
 
 <b>IMPORTANT</b>: If an allowance for the spender does not currently exist, this transaction 
 behaves like an allowance approval.

<!-- tabs:start -->

#### ** Java **

```java
new AccountAllowanceAdjustTransaction()
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .setSpenderAccountId(accountId)
    .setTokenId(tokenId)
    .setAmount(10)
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await new AccountAllowanceAdjustTransaction()
        .setNodeAccountIds([response.nodeId])
        .setSpenderAccountId(accountId)
        .setTokenId(tokenId)
        .setAmount(10)
        .execute(client)
).getReceipt(client);
```

- `Duration` is `number` and is the number of seconds

#### ** Go **

```go
response, err := hedera.NewAccountAllowanceAdjustTransaction().
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetSpenderAccountID(accountID).
    SetTokenID(tokenID).
    SetAmount(10).
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

##### `spenderAccountId`: [`AccountId`](reference/cryptography/AccountId.md)

The account ID of the spender of the hbar/token allowance.

---

##### `tokenId`: [`TokenId`](reference/token/TokenId.md)

The token that the allowance pertains to. If this field is omitted, the adjustment
will be made against the spender's hbar allowance with the payer account.

---

##### `amount`: `Int64`

The amount to adjust the current allowance balance by. If this value is negative
the approved allowance will be decreased. The adjusted allowance balance cannot
exceed the total supply of the token nor can it be negative.

---
