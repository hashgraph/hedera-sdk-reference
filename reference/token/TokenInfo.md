> class `TokenInfo`

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): `TokenInfo`

---

### Methods

##### `toBytes` (): `bytes`

---

### Fields

##### `tokenId`: `TokenId`

---

##### `name`: `String`

---

##### `symbol`: `String`

---

##### `decimals`: `Uint64`

---

##### `totalSupply`: `Uint64`

---

##### `treasuryAccountId`: `?AccountId`

---

##### `adminKey`: `?Key`

---

##### `kycKey`: `?Key`

---

##### `freezeKey`: `?Key`

---

##### `wipeKey`: `?Key`

---

##### `supplyKey`: `?Key`

---

##### `pauseKey`: [`Key`](reference/cryptography/Key.md)

The Key which can pause and unpause the Token.

---

##### `defaultFreezeStatus`: `?bool`

---

##### `defaultKycStatus`: `?bool`

---

##### `defaultPauseStatus`: `?bool`

Specifies whether the token is paused or not.
 - `null`: PauseNotApplicable
 - `false`: Unpaused
 - `true`: Paused

---

##### `isDeleted`: `bool`

---

##### `autoRenewAccountId`: `?AccountId`

---

##### `expirationTime`: `Timestamp`

---

##### `autoRenewPeriod`: `Duration`

---
