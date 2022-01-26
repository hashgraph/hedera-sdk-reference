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
var key = PrivateKey.generate();

new TransferTransaction()
    .addHbarTransfer(new AccountId(1451), new Hbar(10)) // 10 hbars
    .addHbarTransfer(client.getOperatorAccountId()), new Hbar(10).negate()) // -10 hbars
    .execute(client) // TransactionResponse
    .getReceipt(client); // TransactionReceipt
```

#### ** JavaScript **

```javascript
const key = PrivateKey.generate();

const transaction = new TransferTransaction()
    .addHbarTransfer(new AccountId(1451), new Hbar(10)) // 10 hbars
    .addHbarTransfer(client.operatorAccountId), new Hbar(10).negate()); // -10 hbars

const response = await transferTransaction.execute(client) // TransactionResponse;
const receipt = await response.getReceipt(client) // TransactionReceipt;
```

- `Duration` is `number` and is the number of seconds

#### ** Go **

```go
newKey := hedera.GeneratePrivateKey()

response, err := hedera.NewTransferTransaction().
    AddHbarTransfer(AccountID{Account: 1451}, hedera.NewHbar(10)). // 10 Hbars
    AddHbarTransfer(client.GetOperatorAccountID(), hedera.NewHbar(10).Negate()). // -10 Hbars
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

### Methods

##### `addHbarTransfer` ( `accountId`: [`AccountId`](reference/cryptocurrency/AccountId.md), `amount`: [`Hbar`](reference/Hbar.md) ): `TransferTransaction`

Add an Hbar transfer

---

##### `getHbarTransfers` (): `Map` < `[`AccountId`](reference/cryptocurrency/AccountId.md), [`Hbar`](reference/Hbar.md) >

The Hbar transfers

---

##### `addTokenTransfer` ( `tokenId`: [`TokenId`](reference/token/TokenId.md), `accountId`: `[`AccountId`](reference/cryptocurrency/AccountId.md), `amount`: `Uint64` ) ): `TransferTransaction`

Add a fungible token transfer

---

##### `addTokenTransferWithDecimals` ( `tokenId`: [`TokenId`](reference/token/TokenId.md), `accountId`: `[`AccountId`](reference/cryptocurrency/AccountId.md), `amount`: `Uint64`, `decimals`: `Uint32` ) ): `TransferTransaction`

Add a fungible token transfer with an expected decimals field

---

##### `getTokenIdDecimals` (): `Map` < [`TokenId`](reference/token/TokenId.md), `Uint32` >

The expected decimals per token ID

---

##### `getTokenTransfers` (): `Map` < [`TokenId`](reference/token/TokenId.md), `Map` < `[`AccountId`](reference/cryptocurrency/AccountId.md), `Uint64` > >

The fungible token transfers

---

##### `addNftTransfer` ( `nftId`: [`NftId`](reference/token/NftId.md), `sender`: [`AccountId`](reference/cryptocurrency/AccountId.md), `reciever`: [`AccountId`](reference/cryptocurrency/AccountId.md) ): `TransferTransaction`

Add a non-fungible token transfer

---

##### `getTokenNftTransfers` (): `Map` < [`TokenId`](reference/token/TokenId.md), `List` < `[`TokenNftTransfer`](reference/token/TokenNftTransfer.md) > >

The non-fungible token transfers

---
