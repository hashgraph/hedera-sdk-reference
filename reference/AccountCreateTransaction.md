# class `AccountCreateTransaction`

Create a new Hedera™ crypto-currency account.

## Properties

### [`key: Key`](Key.md)

This is the key that must sign each transfer out of the account.

If `receiverSignatureRequired` is true, then the key must also sign
any transfer into the account.

### `initialBalance: Hbar`

The initial number of hbars to put into the account.

Defaults to `0`.

### `receiverSignatureRequired: bool`

If true, this account's key must sign any transaction depositing
into this account (in addition to all withdrawals).

Defaults to `false`.

### `autoRenewPeriod: Duration`

The account is charged to extend its expiration date every this many seconds.

If it doesn't have enough balance, it extends as long as possible.
If it is empty when it expires, then it is deleted.

Defaults to 90 days (or 7,776,000 seconds).

### `proxyAccountId: ?AccountId`

ID of the account to which this account is proxy staked.

If `proxyAccountId` is null, or is an invalid account, or is an
account that isn't a node, then this account is automatically proxy staked
to a node chosen by the network, but without earning payments.

If the `proxyAccountId` account refuses to accept proxy staking, or if it is
not currently running a node, then it will behave as
if `proxyAccountId` was null.

## Declaration

```typescript
interface AccountCreateTransaction extends Transaction {
    constructor();

    getKey(): Key | null;
    setKey(key: Key): this;

    getInitialBalance(): Hbar;
    setInitialBalance(initialBalance: Hbar): this;

    getAutoRenewPeriod(): Duration;
    setAutoRenewPeriod(autoRenewPeriod: Duration): this;

    getProxyAccountId(): AccountId | null;
    setProxyAccountId(proxyAccountId: AccountId): this;

    getReceiverSignatureRequired(): bool;
    setReceiverSignatureRequired(receiverSignatureRequired: bool): this;
}
```

## Examples

#### Java

```java
var newKey = PrivateKey.generate();

var newAccountId = new AccountCreateTransaction()
    .setKey(newKey)
    .setInitialBalance(new Hbar(10)) // 10 hbars
    .execute(client) // TransactionResponse
    .getReceipt(client) // TransactionReceipt
    .accountId // Optional<AccountId>
    .orElseThrow(); // AccountId
```

#### JavaScript

```js
const newKey = PrivateKey.generate();

const accountCreateTransaction = new AccountCreateTransaction()
  .setKey(newKey)
  .setInitialBalance(new Hbar(10)); // 10 hbars

const transactionResponse = await accountCreateTransaction.execute(client);

const transactionReceipt = await transactionResponse.getReceipt(client);

const newAccountId = transactionReceipt.accountId;
```

- `Duration` is `number` and is the number of seconds

#### Go

```go
newKey := hedera.GeneratePrivateKey()
newAccountID := NewAccountCreateTransaction().
    SetKey(newKey).
    SetInitialBalance(10 * hedera.Hbar) // 10 Hbars
    Execute(client). // TransactionResponse
    GetReceipt(client). // TransactionReceipt
    AccountID() // AccountID
```
