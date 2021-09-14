> class `ContractInfo`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`fromBytes`](#frombytes-data-bytes-contractinfo) | ✅ | ✅ | ✅
| [`contractId`](#contractid-contractid) | ✅ | ✅ | ✅
| [`contractMemo`](#contractmemo-string) | ✅ | ✅ | ✅
| [`accountId`](#accountid-accountid) | ✅ | ✅ | ✅
| [`contractAccountId`](#contractaccountid-string) | ✅ | ✅ | ✅
| [`adminKey`](#adminkey-key) | ✅ | ✅ | ✅
| [`expirationTime`](#expirationtime-timestamp) | ✅ | ✅ | ✅
| [`autoRenewPeriod`](#autorenewperiod-duration) | ✅ | ✅ | ✅
| [`storage`](#storage-uint64) | ✅ | ✅ | ✅
| [`balance`](#balance-hbar) | ✅ | ✅ | ✅
| [`isDeleted`](#isdeleted-bool) | ✅ | ✅ | ✅
| [`tokenRelantionships`](#tokenrelationships-map-lt-tokenid-tokenrelationship-gt) | ✅ | ✅ | ✅
| [`toBytes`](#tobytes-bytes) | ✅ | ✅ | ✅
| [`toString`](#tostring-string) | ✅ | ✅ | ✅

</details>

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): `ContractInfo`

---

### Methods

##### `toBytes` (): `bytes`

---

##### `toString` (): `String`

---

### Properties

##### `contractId`: [`ContractId`](reference/contract/ContractId.md)

ID of the contract instance.

---

##### `contractMemo`: `String`

The memo associated with the contract (max 100 bytes).

---

##### `accountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

ID of the cryptocurrency account owned by the contract instance.

---

##### `contractAccountId`: `String`

ID of both the contract instance and the cryptocurrency account owned by the contract instance, in the format used by Solidity.

---

##### `adminKey`: [`Key`](reference/cryptography/Key.md)

The state of the instance and its fields can be modified arbitrarily if `adminKey` signs a transaction to modify it.
If this is null, then such modifications are not possible, and there is no administrator that can override the normal operation of this smart contract instance.
Note that if it is created with no admin keys, then there is no administrator to authorize changing the admin keys, so there can never be any admin keys for that instance.

---

##### `expirationTime`: `Timestamp`

The current time at which this contract instance (and its account) is set to expire.

---

##### `autoRenewPeriod`: `Duration`

The expiration time will extend every this many seconds.
If there are insufficient funds, then it extends as long as possible.
If the account is empty when it expires, then it is deleted.

---

##### `storage`: `Uint64`

Number of bytes of storage being used by this instance (which affects the cost to extend the expiration time).

---

##### `balance`: [`Hbar`](reference/Hbar.md)

The current balance, in tinybars.

---

##### `isDeleted`: `bool`

Whether the contract has been deleted.

---

##### `tokenRelationships`: `Map` < [`TokenId`](reference/token/TokenId.md), [`TokenRelationship`](reference/token/TokenRelationship.md) >

The tokens associated to the contract.

---
