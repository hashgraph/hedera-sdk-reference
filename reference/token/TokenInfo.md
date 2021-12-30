> class `TokenInfo`

The metadata about a Token instance

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): `TopicInfo`

Deserialize a [`TokenInfo`](#) from its the protobuf representation.

---

### Methods

##### `toBytes` (): `bytes`

Serialize the [`TokenInfo`](#) into its protobuf representation.

---

### Fields

##### `tokenId`: [`TokenId`](reference/token/TokenId.md)

ID of the token instance

---

##### `name`: `string`

The name of the token. It is a string of ASCII only characters

---

##### `symbol`: `string`

The symbol of the token. It is a UTF-8 capitalized alphabetical string

---

##### `decimals`: `Uint32`

The number of decimal places a token is divisible by. Always 0 for tokens of type
NON\_FUNGIBLE\_UNIQUE

---

##### `totalSupply`: `Uint64`

For tokens of type FUNGIBLE\_COMMON - the total supply of tokens that are currently in
circulation. For tokens of type NON\_FUNGIBLE\_UNIQUE - the number of NFTs created of this
token instance

---

##### `treasuryAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The ID of the account which is set as Treasury

---

##### `adminKey`: [`Key`](reference/cryptography/Key.md)

The key which can perform update/delete operations on the token. If empty, the token can be
perceived as immutable (not being able to be updated/deleted)

---

##### `kycKey`: [`Key`](reference/cryptography/Key.md)

The key which can grant or revoke KYC of an account for the token's transactions. If empty,
KYC is not required, and KYC grant or revoke operations are not possible.

---

##### `freezeKey`: [`Key`](reference/cryptography/Key.md)

The key which can freeze or unfreeze an account for token transactions. If empty, freezing is
not possible

---

##### `wipeKey`: [`Key`](reference/cryptography/Key.md)

The key which can wipe token balance of an account. If empty, wipe is not possible

---

##### `supplyKey`: [`Key`](reference/cryptography/Key.md)

The key which can change the supply of a token. The key is used to sign Token Mint/Burn
operations

---

##### `pauseKey`: [`Key`](reference/cryptography/Key.md)

The Key which can pause and unpause the Token.

---

##### `feeScheduleKey`: [`Key`](reference/cryptography/Key.md)

The key which can change the custom fee schedule of the token; if not set, the fee schedule
is immutable

---

##### `defaultFreezeStatus`: `bool/`

The default Freeze status (not applicable, frozen or unfrozen) of Hedera accounts relative to
this token. FreezeNotApplicable is returned if Token Freeze Key is empty. Frozen is returned
if Token Freeze Key is set and defaultFreeze is set to true. Unfrozen is returned if Token
Freeze Key is set and defaultFreeze is set to false

 - `null`: FreezeNotApplicable
 - `false`: Unfrozen
 - `true`: Frozen

---

##### `defaultKycStatus`: `bool?`

The default KYC status (KycNotApplicable or Revoked) of Hedera accounts relative to this
token. KycNotApplicable is returned if KYC key is not set, otherwise Revoked

 - `null`: KycNotApplicable
 - `false`: Revoked
 - `true`: Granted

---

##### `pauseStatus`: `bool?`

Specifies whether the token is paused or not. PauseNotApplicable is returned if pauseKey is not set.

 - `null`: PauseNotApplicable
 - `false`: Unpaused
 - `true`: Paused

---

##### `isDeleted`: `bool`

Specifies whether the token was deleted or not

---

##### `autoRenewAccountId`: `AccountID`

An account which will be automatically charged to renew the token's expiration, at
autoRenewPeriod interval

---

##### `autoRenewPeriod`: `Duration`

The interval at which the auto-renew account will be charged to extend the token's expiry

---

##### `expiry`: `Timestamp`

The epoch second at which the token will expire

---

##### `tokenMemo`: `string`

The memo associated with the token

---

##### `tokenType`: `TokenType`

The token type

---

##### `supplyType`: `TokenSupplyType`

The token supply type

---

##### `maxSupply`: `Uint64`

For tokens of type FUNGIBLE\_COMMON - The Maximum number of fungible tokens that can be in
circulation. For tokens of type NON\_FUNGIBLE\_UNIQUE - the maximum number of NFTs (serial
numbers) that can be in circulation

---

##### `customFee`: [`CustomFee`](reference/token/CustomFee.md)

The custom fees to be assessed during a CryptoTransfer that transfers units of this token

---

##### `ledgerId`: [`LedgerId`](reference/LedgerId.md)

The ID of the ledger which returned this response

---
