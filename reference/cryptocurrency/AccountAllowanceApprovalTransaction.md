> class `AccountAllowanceApproveTransaction` extends [`Transaction`](reference/core/Transaction.md)

Creates one or more hbar/token approved allowances <b>relative to the payer account of this
transaction</b>. Each allowance grants a spender the right to transfer a pre-determined
amount of the payer's hbar/token to any other account of the spender's choice.

(So if account <tt>0.0.X</tt> pays for this transaction, then at consensus each spender
account will have new allowances to spend hbar or tokens from <tt>0.0.X</tt>).

<!-- tabs:start -->

#### ** Java **

```java
new AccountAllowanceApproveTransaction()
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .addHbarApprove(accountId, Hbar.fromTinybars(10))
    .addTokenApprove(tokenId, accountId, 10)
    .addTokenNftApprove(tokenId, accountId, null)
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await new AccountAllowanceApproveTransaction()
        .setNodeAccountIds([response.nodeId])
        .addHbarApprove(accountId, Hbar.fromTinybars(10))
        .addTokenApprove(tokenId, accountId, 10)
        .addTokenApprove(tokenId, accountId, null)
        .execute(client)
).getReceipt(client);
```

- `Duration` is `number` and is the number of seconds

#### ** Go **

```go
newKey := hedera.GeneratePrivateKey()

resp, err := hedera.NewAccountAllowanceApproveTransaction().
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    AddHbarApprove(accountID, HbarFromTinybars(10)).
    AddTokenApprove(tokenID, accountID, 10).
    AddTokenApprove(tokenID, accountID, null).
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

##### `addHbarApprove`: ( `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `amount`: [`Hbar`](reference/Hbar.md)) : `AccountAllowanceApproveTransaction`

Add a Hbar allowance

---

##### `getHbarAllowances` (): `List` < [`HbarAllowance`](reference/cryptocurrency/HbarAllowance.md)

Get the current list of hbar approves for this transaction.

---

##### `addTokenApprove`: ( `tokenId`: [`TokenId`](reference/token/TokenId.md), `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `amount`: `Uint64`) : `AccountAllowanceApproveTransaction`

Add a fungible token approve

---

##### `getTokenAllowances` (): `List` < [`TokenAllowance`](reference/cryptocurrency/TokenAllowance.md)

Get the current list of hbar approves for this transaction.

---

##### `addTokenNftApprove`: ( `nftId`: [`NftId`](reference/token/NftId.md), `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md)) : `AccountAllowanceApproveTransaction`

Add a non-fungible token approve

---

##### `addAllTokenNftApprove`: ( `tokenId`: [`TokenId`](reference/token/TokenId.md), `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md)) : `AccountAllowanceApproveTransaction`

Add all non-fungible tokens to approve

---

##### `getTokenNftAllowances`(): `List` < [`TokenNftAllowance`](reference/cryptocurrency/TokenNftAllowance.md)

Get the list of all non-fungible token approves for this transaction

---
