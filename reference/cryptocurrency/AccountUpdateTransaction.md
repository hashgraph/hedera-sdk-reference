# `AccountUpdateTransaction`

> class `AccountUpdateTransaction` extends [`Transaction`](reference/core/Transaction.md)

<!-- tabs:start -->

#### ** Java **

```java
new AccountUpdateTransaction()
    .setAccountId(accountId)
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .setKey(key2.getPublicKey())
    .freezeWith(client)
    .sign(key1)
    .sign(key2)
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
const newKey = PrivateKey.generate();

response = await (
    await (
        await new AccountUpdateTransaction()
            .setAccountId(account)
            .setKey(key2.publicKey)
            .setNodeAccountIds([response.nodeId])
            .setMaxTransactionFee(new Hbar(1))
            .freezeWith(client)
            .sign(key1)
    ).sign(key2)
).execute(client);
const receipt = await response.getReceipt(client);

const newAccountId = receipt.accountId;
```

#### ** Go **

```go
transaction, err := hedera.NewAccountUpdateTransaction().
    SetAccountID(accountID).
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetKey(newKey2.PublicKey()).
    FreezeWith(client)
if err != nil {
    println(err.Error())
}

transaction.Sign(previousKey)
transaction.Sign(newKey2)

response, err = tx.Execute(client)
if err != nil {
    println(err.Error())
}

receipt, err := response.GetReceipt(client)
if err != nil {
    println(err.Error())
}

newAccountId := *receipt.accountId;
```

<!-- tabs:end -->

### Constructor

##### `constructor`()

---

### Properties

##### `AccountId`: [`AccountId`](reference/cryptography/AccountId.md)

---

##### `key`: [`Key`](reference/cryptography/Key.md)

This is the key that must sign each transfer out of the account.

If `receiverSignatureRequired` is true, then the key must also sign
any transfer into the account.

---

##### `receiverSignatureRequired`: `bool`

If true, this account's key must sign any transaction depositing
into this account (in addition to all withdrawals).

Defaults to `false`.

---

##### `autoRenewPeriod`: `Duration`

The account is charged to extend its expiration date every this many seconds.

If it doesn't have enough balance, it extends as long as possible.
If it is empty when it expires, then it is deleted.

Defaults to 90 days (or 7,776,000 seconds).

---

##### `proxyAccountId`: [`AccountId`](reference/AccountId.md)

ID of the account to which this account is proxy staked.

If `proxyAccountId` is null, or is an invalid account, or is an
account that isn't a node, then this account is automatically proxy staked
to a node chosen by the network, but without earning payments.

If the `proxyAccountId` account refuses to accept proxy staking, or if it is
not currently running a node, then it will behave as
if `proxyAccountId` was null.

---

##### `expirationTime`: `Timestamp`

---
