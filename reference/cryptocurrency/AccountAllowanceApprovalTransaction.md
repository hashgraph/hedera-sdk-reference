> class `AccountAllowanceApprovalTransaction` extends [`Transaction`](reference/core/Transaction.md)

Creates one or more hbar/token approved allowances <b>relative to the payer account of this
transaction</b>. Each allowance grants a spender the right to transfer a pre-determined 
amount of the payer's hbar/token to any other account of the spender's choice. 

(So if account <tt>0.0.X</tt> pays for this transaction, then at consensus each spender 
account will have new allowances to spend hbar or tokens from <tt>0.0.X</tt>). 

<!-- tabs:start -->

#### ** Java **

```java
new AccountAllowanceApprovalTransaction()
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .addHbarApproval(accountId, Hbar.fromTinybars(10))
    .addTokenApproval(tokenId, accountId, 10)
    .addTokenApproval(tokenId, accountId, null)
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await new AccountAllowanceApprovalTransaction()
        .setNodeAccountIds([response.nodeId])
        .addHbarApproval(accountId, Hbar.fromTinybars(10))
        .addTokenApproval(tokenId, accountId, 10)
        .addTokenApproval(tokenId, accountId, null)
        .execute(client)
).getReceipt(client);
```

- `Duration` is `number` and is the number of seconds

#### ** Go **

```go
newKey := hedera.GeneratePrivateKey()

resp, err := hedera.NewAccountAllowanceApprovalTransaction().
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    AddHbarApproval(accountID, HbarFromTinybars(10)).
    AddTokenApproval(tokenID, accountID, 10).
    AddTokenApproval(tokenID, accountID, null).
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

### Constructor

##### `constructor`()

---

### Methods

##### `addHbarApproval` ( `accountId`: [`AccountId`](reference/cryptocurrency/AccountId.md), `amount`: [`Hbar`](reference/Hbar.md) ): `AccountAccountAllowanceApprovalTransaction`

Add an Hbar approval

---

##### `getHbarApprovals` (): `List` < [`HbarApproval`](reference/cryptography/HbarApproval.md) >

List of hbar allowances approved by the account owner.

---

##### `addTokenApproval` ( `tokenId`: [`TokenId`](reference/token/TokenId.md), `accountId`: `[`AccountId`](reference/cryptocurrency/AccountId.md), `amount`: `Uint64?` ): `AccountAccountAllowanceApprovalTransaction`

Add a token approval

---

##### `getTokenApprovals` (): `List` < [`TokenApproval`](reference/cryptography/TokenApproval.md) >

List of token (fungible or non-fungible) allowances approved by the account owner.

---
