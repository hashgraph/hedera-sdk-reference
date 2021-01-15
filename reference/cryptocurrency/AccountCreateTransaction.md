# `AccountCreateTransaction`

> class `AccountCreateTransaction` extends [`Transaction`](reference/core/Transaction.md)

Create a new Hedera™ crypto-currency account.

The Key field is the key used to sign transactions for this account. If the
account has `receiverSignatureRequired` set to true, then all cryptocurrency
transfers must be signed by this account's key, both for transfers in and out.
If it is false, then only transfers out have to be signed by it. When the
account is created, the payer account is charged enough hbars so that the
new account will not expire for the next autoRenewPeriod seconds.

When it reaches the expiration time, the new account will then be automatically
charged to renew for another autoRenewPeriod seconds. If it does not have
enough hbars to renew for that long, then the remaining hbars are used to
extend its expiration as long as possible. If it is has a zero balance when
it expires, then it is deleted. This transaction must be signed by the payer
account. If `receiverSignatureRequired` is false, then the transaction does not
have to be signed by the keys in the keys field. If it is true, then it must be
signed by them, in addition to the keys of the payer account.

An entity (account, file, or smart contract instance) must be created in a
particular realm. If the realmID is left null, then a new realm will be created
with the given admin key. If a new realm has a null adminKey, then anyone can
create/modify/delete entities in that realm. But if an admin key is given,
then any transaction to create/modify/delete an entity in that realm must be
signed by that key, though anyone can still call functions on smart contract
instances that exist in that realm. A realm ceases to exist when everything
within it has expired and no longer exists.

The current API ignores shardID, realmID, and newRealmAdminKey,
and creates everything in shard 0 and realm 0, with a null key.
Future versions of the API will support multiple realms and multiple shards.

> [!WARNING]
> When creating a new account an existing account will need to fund the initial
> balance and pay for the transaction fee.

<!-- tabs:start -->

#### ** Java **

```java
var key = PrivateKey.generate();

var fileId = new AccountCreateTransaction()
    .setKey(key)
    .setInitialBalance(new Hbar(10)) // 10 hbars
    .execute(client) // TransactionResponse
    .getReceipt(client) // TransactionReceipt
    .accountId // Nullable<AccountId>
```

#### ** JavaScript **

```javascript
const key = PrivateKey.generate();

const transaction = new AccountCreateTransaction({
    key: newKey,
    initialBalance: new Hbar(10),
});

const response = await accountCreateTransaction.execute(client) // TransactionResponse;
const receipt = await response.getReceipt(client) // TransactionReceipt;
const accountId = receipt.accountId // Nullable<AccountId>;
```

- `Duration` is `number` and is the number of seconds

#### ** Go **

```go
newKey := hedera.GeneratePrivateKey()

response, err := hedera.NewAccountCreateTransaction().
    SetKey(newKey).
    SetInitialBalance(10 * hedera.Hbar) // 10 Hbars
    Execute(client) // TransactionResponse
if err != nil {
    println(err.Error())
}

receipt, err := response.GetReceipt(client)
if err != nil {
    println(err.Error())
}

accountID := *receipt.AccountID
```

<!-- tabs:end -->

### Constructor

##### `constructor`()

---

### Properties

##### `key`: [`Key`](reference/cryptography/Key.md)

This is the key that must sign each transfer out of the account.

If `receiverSignatureRequired` is true, then the key must also sign
any transfer into the account.

---

##### `initialBalance`: [`Hbar`](reference/Hbar.md)

The initial number of hbars to put into the account.

Defaults to `0`.

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
