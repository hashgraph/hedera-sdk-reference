> class `AccountUpdateTransaction` extends [`Transaction`](reference/core/Transaction.md)

Change properties for the given account. Any null field is ignored (left unchanged). This
transaction must be signed by the existing key for this account. If the transaction is changing
the key field, then the transaction must be signed by both the old key (from before the change)
and the new key. The old key must sign for security. The new key must sign as a safeguard to
avoid accidentally changing to an invalid key, and then having no way to recover. 

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

The account ID which is being updated in this transaction

---

##### `key`: [`Key`](reference/cryptography/Key.md)

The new key.

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

The duration in which it will automatically extend the expiration period. If it doesn't have
enough balance, it extends as long as possible. If it is empty when it expires, then it is
deleted.

Defaults to 90 days (or 7,776,000 seconds).

---

##### `proxyAccountId`: [`AccountId`](reference/AccountId.md)

Deprecated: with no replacement

ID of the account to which this account is proxy staked. If proxyAccountID is null, or is an
invalid account, or is an account that isn't a node, then this account is automatically proxy
staked to a node chosen by the network, but without earning payments. If the proxyAccountID
account refuses to accept proxy staking , or if it is not currently running a node, then it
will behave as if proxyAccountID was null.

---

##### `expirationTime`: `Timestamp`

The new expiration time to extend to (ignored if equal to or before the current one)

---

##### `accountMemo`: `String`

If set, the new memo to be associated with the account (UTF-8 encoding max 100 bytes)

---

##### `maxAutomaticTokenAssociations`: `Uint32`

The maximum number of tokens that an Account can be implicitly associated with. Up to a 1000
including implicit and explicit associations.

---

##### `stakedNodeAccountId`: `?AccountId`

ID of the account to which this contract is staking.

---

##### `stakedNodeId`: `?Int64`

ID of the node this contract is staked to.

---

##### `declineStakingReward`: `?bool`

If true, the account declines receiving a staking reward. The default value is false.

---
