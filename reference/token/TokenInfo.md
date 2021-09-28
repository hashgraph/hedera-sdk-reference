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

##### `defaultFreezeStatus`: `bool`

---

##### `defaultKycStatus`: `bool`

---

##### `isDeleted`: `bool`

---

##### `autoRenewAccountId`: `?AccountId`

---

##### `expirationTime`: `Timestamp`

---

##### `autoRenewPeriod`: `Duration`

---

##### `pauseKey`: [`Key`](reference/cryptography/Key.md)

The Key which can pause and unpause the Token.

---

##### `pauseStatus`: [`TokenPauseStatus`](reference/token/TokenPauseStatus.md)

Specifies whether the token is paused or not. PauseNotApplicable is returned if pauseKey is not set.

---
