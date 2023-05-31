> class `AccountInfo`

Info about the account (a state proof can be generated for this)

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): [`AccountInfo`](AccountInfo)

Deserialize a [`AccountInfo`](AccountInfo) from its protobuf representation.

### Methods

##### `toBytes` ( ): `bytes`

Serialize the [`AccountInfo`](AccountInfo) into its protobuf representation.

---

### Fields

##### `accountId`: [`AccountId`](AccountId.md)

The account ID for which this information applies

---

##### `accountMemo`: `String`

The memo associated with the account

---

##### `aliasKey`: `PublicKey`

The alias of this account

---

##### `autoRenewPeriod`: `Timestamp`

The duration for expiration time will extend every this many seconds. If there are
insufficient funds, then it extends as long as possible. If it is empty when it expires,
then it is deleted.

Defaults to 90 days (or 7,776,000 seconds).

---

##### `balance`: [`Hbar`](../Hbar.md)

The current balance of account in tinybars

---

##### `contractAccountId`: `String`

The Contract Account ID comprising both the contract instance and the cryptocurrency
account owned by the contract instance, in the format used by Solidity

---

##### `ethereumNonce`: `Uint64`

The ethereum transaction nonce associated with this account.

---

##### `expirationTime`: `Timestamp`

The TimeStamp time at which this account is set to expire.

---

##### `hbarAllowances`: `List` < [`HbarAllowance`](HbarAllowance.md) >

All Hbar allowances approved by the account owner.

---

##### `isDeleted`: `bool`

If true, then this account has been deleted, it will disappear when it expires, and all
transactions for it will fail except the transaction to extend its expiration date

---

##### `isReceiverSignatureRequired`: `bool`

If true, no transaction can transfer to this account unless signed by this account's key.

---

##### `key`: [`Key`](../cryptography/Key.md)

The key for the account, which must sign in order to transfer out, or to modify the
account in any way other than extending its expiration date.

---

##### `ledgerId`: [`LedgerId`](../LedgerId.md)

The ID of the ledger which returned this response

---

##### `liveHashes`: [`LiveHash[]`](/reference/live-hash/LiveHash.md)

All livehashes attached to the account (each of which is a hash along with the
keys that authorized it and can delete it)

---

##### `maxAutomaticTokenAssociations`: `Uint32`

The maximum number of tokens that an Account can be implicitly associated with.

---

##### `ownedNfts`: `Uint64`

The number of NFTs owned by this account

---

##### `proxyAccountId`: [`AccountId`](AccountId.md)

Deprecated: with no replacement

The Account ID of the account to which this is proxy staked. If proxyAccountID is null,
or is an invalid account, or is an account that isn't a node, then this account is
automatically proxy staked to a node chosen by the network, but without earning payments.
If the proxyAccountID account refuses to accept proxy staking , or if it is not currently
running a node, then it will behave as if proxyAccountID was null.

---

##### `proxyReceived`: [`Hbar`](../Hbar.md)

The total number of tinybars proxy staked to this account

---

##### `receiveRecordThreshold`: [`Hbar`](../Hbar.md)

The threshold amount for which an account record is created (and this account charged
for them) for any transaction above this amount.

---

##### `sendRecordThreshold`: [`Hbar`](../Hbar.md)

The threshold amount for which an account record is created (and this account charged
for them) for any send/withdraw transaction.

---

##### `stakingInfo`: [`StakingInfo`](../StakingInfo.md)

Staking metadata for this contract.

---

##### `tokenAllowances`: `List` < [`TokenAllowance`](TokenAllowance.md) >

All fungible token allowances approved by the account owner.

---

##### `tokenNftAllowances`: `List` < [`TokenNftAllowance`](TokenNftAllowance.md) >

All non-fungible token allowances approved by the account owner.

---

##### `tokenRelationships`: `Map<TokenId, TokenRelationship>`

All tokens related to this account.
