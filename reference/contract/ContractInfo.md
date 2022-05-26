> class `ContractInfo`

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): `ContractInfo`

Deserialize a [`ContractInfo`](#) from its the protobuf representation.

---

### Methods

##### `toBytes` (): `bytes`

Serialize the [`ContractInfo`](#) into its protobuf representation.

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

##### `ledgerId`: [`LedgerId`](reference/LedgerId.md)

The ID of the ledger which returned this response

---

##### `stakingInfo`: [`StakingInfo`](reference/StakingInfo.md)

Staking metadata for this contract.

---
