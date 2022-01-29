> class `AccountInfo`

Info about the account (a state proof can be generated for this)

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): [`AccountInfo`](#)

Deserialize a [`AccountInfo`](#) from its protobuf representation.

---

### Methods

##### `toBytes` ( ): `bytes`

Serialize the [`AccountInfo`](#) into its protobuf representation.

---

### Fields

##### `accountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The account ID for which this information applies

---

##### `contractAccountId`: `String`

The Contract Account ID comprising of both the contract instance and the cryptocurrency
account owned by the contract instance, in the format used by Solidity

---

##### `isDeleted`: `bool`

If true, then this account has been deleted, it will disappear when it expires, and all
transactions for it will fail except the transaction to extend its expiration date

---

##### `proxyAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The Account ID of the account to which this is proxy staked. If proxyAccountID is null,
or is an invalid account, or is an account that isn't a node, then this account is
automatically proxy staked to a node chosen by the network, but without earning payments.
If the proxyAccountID account refuses to accept proxy staking , or if it is not currently
running a node, then it will behave as if proxyAccountID was null.

---

##### `proxyReceived`: [`Hbar`](reference/Hbar.md)

The total number of tinybars proxy staked to this account

---

##### `key`: [`Key`](reference/cryptography/Key.md)

The key for the account, which must sign in order to transfer out, or to modify the
account in any way other than extending its expiration date.

---

##### `balance`: [`Hbar`](reference/Hbar.md)

The current balance of account in tinybars

---

##### `isReceiverSignatureRequired`: `bool`

If true, no transaction can transfer to this account unless signed by this account's key.

---

##### `expirationTime`: `Timestamp`

The TimeStamp time at which this account is set to expire.

---

##### `autoRenewPeriod`: `Timestamp`

The duration for expiration time will extend every this many seconds. If there are
insufficient funds, then it extends as long as possible. If it is empty when it expires,
then it is deleted.

Defaults to 90 days (or 7,776,000 seconds).

---

##### `liveHashes`: [`LiveHash[]`](/reference/live-hash/LiveHash.md)

All of the livehashes attached to the account (each of which is a hash along with the
keys that authorized it and can delete it)

---

##### `tokenRelationships`: `Map<TokenId, TokenRelationship>`

All tokens related to this account.

---

##### `accountMemo`: `String`

The memo associated with the account

---

##### `ownedNfts`: `Uint64`

The number of NFTs owned by this account

---

##### `maxAutomaticTokenAssociations`: `Uint32`

The maximum number of tokens that an Account can be implicitly associated with.

---

##### `aliasKey`: `PublicKey`

The alias of this account

---

##### `ledgerId`: [`LedgerId`](reference/LedgerId.md)

The ID of the ledger which returned this response

---

##### `hbarAllowances`: `List` < [`HbarAllowance`](reference/cryptocurrency/HbarAllowance.md) >

All of the hbar allowances approved by the account owner.

---

##### `tokenAllowances`: `List` < [`TokenAllowance`](reference/cryptocurrency/TokenAllowance.md) >

All of the fungible token allowances approved by the account owner.

---

##### `nftAllowances`: `List` < [`TokenNftAllowance`](reference/cryptocurrency/TokenNftAllowance.md) >

All of the non-fungible token allowances approved by the account owner.

---
