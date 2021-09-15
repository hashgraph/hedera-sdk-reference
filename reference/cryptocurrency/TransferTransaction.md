> class `TransferTransaction` extends [`Transaction`](reference/core/Transaction.md)

Transfers cryptocurrency among two or more accounts by making the desired adjustments to their
balances. Each transfer list can specify up to 10 adjustments. Each negative amount is withdrawn
from the corresponding account (a sender), and each positive one is added to the corresponding
account (a receiver). The amounts list must sum to zero. Each amount is a number of tinybars
(there are 100,000,000 tinybars in one hbar).  If any sender account fails to have sufficient
hbars, then the entire transaction fails, and none of those transfers occur, though the
transaction fee is still charged. This transaction must be signed by the keys for all the sending
accounts, and for any receiving accounts that have receiverSigRequired == true. The signatures
are in the same order as the accounts, skipping those accounts that don't need a signature. 

<!-- tabs:start -->

#### ** Java **

```java
var receipt = new TransferTransaction()
    .addHbarTransfer(client.getOperatorAccountId(), Hbar.fromTinybars(-10))
    .addHbarTransfer(AccountId.fromString("0.0.3"), Hbar.fromTinybars(10))
    .addTokenTransfer(tokenID, client.getOperatorAccountId(), -10)
    .addTokenTransfer(tokenID, AccountId.fromString("0.0.3"), 10)
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
const receipt = await (
    await new TransferTransaction()
        .addHbarTransfer(client.operatorAccountId, new Hbar(-10))
        .addHbarTransfer(new AccountId(3), new Hbar(10))
        .addTokenTransfer(tokenID, client.operatorAccountId, -10)
        .addTokenTransfer(tokenID, new AccountId(3), 10)
        .execute(client)
).getReceipt(client);
```

#### ** Go **

```go
resp, err := hedera.NewTransferTransaction().
    AddHbarTransfer(client.GetOperatorAccountID(), NewHbar(-1)).
    AddHbarTransfer(AccountID{Account: 3}, NewHbar(1)).
    AddTokenTransfer(tokenID, client.GetOperatorAccountID(), -10).
    AddTokenTransfer(tokenID, accountID, 10).
    Execute(client)
if err != nil {
    println(err.Error())
}

receipt, err = resp.GetReceipt(client)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Constructor

##### `constructor`()

---

### Properties

##### `hbarTransfers`: `Map` < [`AccountId`](reference/cryptocurrency/AccountId.md) , [`Hbar`](reference/Hbar.md) >

The desired hbar balance adjustments

---

##### `tokenTransfers`: `Map` < [`TokenId`](reference/token/TokenId.md) , `Map` < [`AccountId`](reference/cryptocurrency/AccountId.md) , `Long` > >

The desired token unit balance adjustments; if any custom fees are assessed, the ledger will
try to deduct them from the payer of this CryptoTransfer, resolving the transaction to
INSUFFICIENT\_PAYER\_BALANCE\_FOR\_CUSTOM\_FEE if this is not possible

A list of token IDs and amounts representing the transferred out (negative) or into (positive)
amounts, represented in the lowest denomination of the token

Applicable to tokens of type FUNGIBLE\_COMMON. Multiple list of AccountAmounts, each of which
has an account and amount

---

##### `nftTransfers`: `Map`< [`AccountId`](reference/cryptocurrency/AccountId.md), [`Hbar`](reference/Hbar.md)>`

Applicable to tokens of type NON\_FUNGIBLE\_UNIQUE. Multiple list of NftTransfers, each of
which has a sender and receiver account, including the serial number of the NFT

---
