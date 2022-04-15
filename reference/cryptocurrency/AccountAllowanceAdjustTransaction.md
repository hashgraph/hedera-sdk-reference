> class `AccountAllowanceAdjustTransaction` extends [`Transaction`](reference/core/Transaction.md)

<b>WARNING</b>: This class has been **deprecated** and is no longer supported by the Hedera protobufs.


 Modifies or creates the hbar/token allowance for a spender <b>relative to the payer account
 of this transaction</b>.

 (So if account <tt>0.0.X</tt> pays for this transaction, then at consensus the spender
 account will have new allowances to spend hbar or tokens from <tt>0.0.X</tt>).

 <b>IMPORTANT</b>: If an allowance for the spender does not currently exist, this transaction
 behaves like an allowance approval.

<!-- tabs:start -->

#### ** Java **

```java
new AccountAllowanceAdjustTransaction() .setNodeAccountIds(Collections.singletonList(response.nodeId)) .addHbarAllowance(accountId, Hbar.fromTinybars(10))
    .addTokenAllowance(tokenId, accountId, 10)
    .addAllTokenNftAllowance(tokenId, accountId)
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await new AccountAllowanceAdjustTransaction()
        .setNodeAccountIds([response.nodeId])
        .addHbarAllowance(accountId, Hbar.fromTinybars(10))
        .addTokenAllowance(tokenId, accountId, 10)
        .addAllTokenNftAllowance(tokenId, accountId)
        .execute(client)
).getReceipt(client);
```

- `Duration` is `number` and is the number of seconds

#### ** Go **

```go
response, err := hedera.NewAccountAllowanceAdjustTransaction().
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    AddHbarAllowance(accountId, Hbar.fromTinybars(10)).
    AddTokenAllowance(tokenId, accountId, 10).
    AddAllTokenNftAllowance(tokenId, accountId).
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

### Methods

##### `addHbarAllowance`: ( `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `amount`: [`Hbar`](reference/Hbar.md)) : `AccountAllowanceAdjustTransaction`

Add a Hbar allowance

Transaction fee payer is implicitly the allowance owner.

Deprecated: use `[grant|revoke]HbarAllowance` instead.

---

##### `grantHbarAllowance`: ( `ownerAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `amount`: [`Hbar`](reference/Hbar.md)) : `AccountAllowanceAdjustTransaction`

Increase an Hbar Allowance.

---

##### `revokeHbarAllowance`: ( `ownerAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `amount`: [`Hbar`](reference/Hbar.md)) : `AccountAllowanceAdjustTransaction`

Decrease an Hbar Allowance.

---

##### `getHbarAllowances`(): `List` < [`HbarAllowance`](references/cryptocurrency/HbarAllowance.md) >

Get the current list of hbar allowances for this transaction.

---

##### `addTokenAllowance`: ( `tokenId`: [`TokenId`](reference/token/TokenId.md), `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `amount`: `Uint64`) : `AccountAllowanceAdjustTransaction`

Add a fungible token allowance

Transaction fee payer is implicitly the allowance owner.

Deprecated: use `[grant|revoke]TokenAllowance` instead.

---

##### `grantTokenAllowance`: ( `tokenId`: [`TokenId`](reference/token/TokenId.md), `ownerAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `amount`: `Uint64`) : `AccountAllowanceAdjustTransaction`

Increase a fungible token allowance.

---

##### `revokeTokenAllowance`: ( `tokenId`: [`TokenId`](reference/token/TokenId.md), `ownerAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `amount`: `Uint64`) : `AccountAllowanceAdjustTransaction`

Decrease a fungible token allowance.

---

##### `getTokenAllowances`: `List` < [`TokenAllowance`](reference/cryptocurrency/TokenAllowance.md)

Get the current list of hbar allowances for this transaction.

---

##### `addTokenNftAllowance`: ( `nftId`: [`NftId`](reference/token/NftId.md), `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md)) : `AccountAllowanceAdjustTransaction`

Add a non-fungible token allowance

Transaction fee payer is implicitly the allowance owner.

Deprecated: use `[grant|revoke]TokenNftAllowance` instead.

---

##### `grantTokenNftAllowance`: ( `nftId`: [`NftId`](reference/token/NftId.md), `ownerAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md)) : `AccountAllowanceAdjustTransaction`

Add serials to a non-fungible token allowance.

---

##### `revokeTokenNftAllowance`: ( `nftId`: [`NftId`](reference/token/NftId.md), `ownerAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md)) : `AccountAllowanceAdjustTransaction`

Remove serials from a non-fungible token allowance.

---

##### `addAllTokenNftAllowance`: ( `tokenId`: [`TokenId`](reference/token/TokenId.md), `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md)) : `AccountAllowanceAdjustTransaction`

Add all non-fungible tokens to allowance

Transaction fee payer is implicitly the allowance owner.

Deprecated: use `[grant|revoke]TokenNftAllowanceAllSerials` instead.

---

##### `grantTokenNftAllowanceAllSerials`: ( `tokenId`: [`TokenId`](reference/token/TokenId.md), `ownerAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md)) : `AccountAllowanceAdjustTransaction`

Add all serials to a non-fungible token allowance.

---

##### `revokeTokenNftAllowanceAllSerials`: ( `tokenId`: [`TokenId`](reference/token/TokenId.md), `ownerAccountId` : [`AccountId`](reference/cryptography/AccountId.md), `spenderAccountId` : [`AccountId`](reference/cryptography/AccountId.md)) : `AccountAllowanceAdjustTransaction`

Remove all serials from a non-fungible token allowance.

---

##### `getTokenNftAllowances`: () `List` < [`TokenNftAllowance`](reference/cryptocurrency/TokenNftAllowance.md)

Get the list of all non-fungible token allowances for this transaction

---
