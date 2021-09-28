> class `TokenCreateTransaction` extends [`Transaction`](reference/core/Transaction.md)

Create a new token. After the token is created, the Token ID for it is in the receipt.
The specified Treasury Account is receiving the initial supply of tokens as-well as the tokens from the Token Mint
operation once executed. The balance of the treasury account is decreased when the Token Burn operation is executed.

The supply that is going to be put in circulation is going to be the initial supply provided. The maximum supply a token
can have is 2^63-1.
Example:
Token A has initial supply set to 10_000 and decimals set to 2. The tokens that will be put into circulation are going be 100.
Token B has initial supply set to 10_012_345_678 and decimals set to 8. The number of tokens that will be put into
circulation are going to be 100.12345678

Creating immutable token: Token can be created as immutable if the adminKey is omitted. In this case, the name, symbol,
treasury, management keys, expiry and renew properties cannot be updated. If a token is created as immutable, anyone is
able to extend the expiry time by paying the fee.

> [!WARNING]
> When creating a new token an existing token will need to pay for the transaction fee.

<!-- tabs:start -->

#### ** Java **

```java
newTokenId = new TokenCreateTransaction()
    .setName("ffff")
    .setSymbol("F")
    .setDecimals(3)
    .setInitialSupply(1000000)
    .setTreasury(OPERATOR_ID)
    .setAdminKey(OPERATOR_KEY.publicKey)
    .setFreezeKey(OPERATOR_KEY.publicKey)
    .setWipeKey(OPERATOR_KEY.publicKey)
    .setKycKey(OPERATOR_KEY.publicKey)
    .setSupplyKey(OPERATOR_KEY.publicKey)
    .setFreezeDefault(false)
    .setExpirationTime(Instant.now().plus(Duration.ofDays(90)))
    .execute(client)
    .getReceipt(client)
    .tokenId;
```

#### ** JavaScript **

```js
response = await new TokenCreateTransaction()
    .setTokenName("ffff")
    .setTokenSymbol("F")
    .setDecimals(3)
    .setInitialSupply(1000000)
    .setTreasuryAccountId(operatorId)
    .setAdminKey(operatorKey)
    .setKycKey(operatorKey)
    .setFreezeKey(operatorKey)
    .setWipeKey(operatorKey)
    .setSupplyKey(operatorKey)
    .setFreezeDefault(false)
    .execute(client);

tokenId = (await response.getReceipt(client)).tokenId;
```

- `Duration` is `number` and is the number of seconds

#### ** Go **

```go
response, err := hedera.NewTokenCreateTransaction().
    SetTokenName("ffff").
    SetTokenSymbol("F").
    SetDecimals(3).
    SetInitialSupply(1000000).
    SetTreasuryAccountID(client.GetOperatorAccountID()).
    SetAdminKey(client.GetOperatorPublicKey()).
    SetFreezeKey(client.GetOperatorPublicKey()).
    SetWipeKey(client.GetOperatorPublicKey()).
    SetKycKey(client.GetOperatorPublicKey()).
    SetSupplyKey(client.GetOperatorPublicKey()).
    SetFreezeDefault(false).
    Execute(client)
if err != nil {
    println(err.Error())
}

receipt, err := response.GetReceipt(client)
if err != nil {
    println(err.Error())
}

tokenID := *receipt.TokenID
```

<!-- tabs:end -->

### Constructor

##### `constructor`()

---

### Properties

##### `name`: `String`

The publicly visible name of the token, specified as a string of only ASCII characters

---

##### `symbol`: `String`

The publicly visible token symbol. It is UTF-8 capitalized alphabetical string identifying the token

---

##### `decimals`: `Uint64`

The number of decimal places a token is divisible by. This field can never be changed!

---

##### `initialSupply`: `Uint64`

Specifies the initial supply of tokens to be put in circulation. The initial supply is sent to the Treasury Account.
The supply is in the lowest denomination possible.

Defaults to `0`.

---

##### `treasuryAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The account which will act as a treasury for the token. This account will receive the specified initial supply

---

##### `adminKey`: [`Key`](reference/cryptography/Key.md)

The key which can perform update/delete operations on the token. If empty, the token can be perceived as immutable
(not being able to be updated/deleted)

Note: This key **MUST** sign the transaction if present.

---

##### `kycKey`: [`Key`](reference/cryptography/Key.md)

The key which can grant or revoke KYC of an account for the token's transactions. If empty, KYC is not required,
and KYC grant or revoke operations are not possible.

---

##### `freezeKey`: [`Key`](reference/cryptography/Key.md)

The key which can sign to freeze or unfreeze an account for token transactions. If empty, freezing is not possible

---

##### `wipeKey`: [`Key`](reference/cryptography/Key.md)

The key which can wipe the token balance of an account. If empty, wipe is not possible

---

##### `supplyKey`: [`Key`](reference/cryptography/Key.md)

The key which can change the supply of a token. The key is used to sign Token Mint/Burn operations

Note: This key **MUST** sign the transaction if present.

---

##### `freezeDefault`: [`boolean`](reference/Hbar.md)

The default Freeze status (frozen or unfrozen) of Hedera accounts relative to this token. If true, an account must
be unfrozen before it can receive the token

---

##### `expirationTime`: [`Timestamp`](reference/Timestamp.md)

The epoch second at which the token should expire; if an auto-renew account and period are specified,
this is coerced to the current epoch second plus the autoRenewPeriod

---

##### `autoRenewAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

An account which will be automatically charged to renew the token's expiration, at autoRenewPeriod interval

Note: This `AccountId` **MUST** sign the transaction if present.

---

##### `autoRenewPeriod`: [`Duration`](reference/Duration.md)

The interval at which the auto-renew account will be charged to extend the token's expiry

---

##### `pauseKey`: [`Key`](reference/cryptography/Key.md)

The Key which can pause and unpause the Token. If Empty the token pause status defaults to
PauseNotApplicable, otherwise Unpaused.

---
