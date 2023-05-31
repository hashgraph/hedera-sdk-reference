> class `ContractInfo`

Current information on the smart contract instance, including its balance.

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): `ContractInfo`

Deserialize a [`ContractInfo`](ContractInfo) from its protobuf representation.

---

### Methods

##### `toBytes` (): `bytes`

Serialize the [`ContractInfo`](ContractInfo) into its protobuf representation.

---

### Properties

##### `accountId`: [`AccountId`](../cryptocurrency/AccountId.md)

ID of the cryptocurrency account owned by the contract instance.

---

##### `adminKey`: [`Key`](../cryptography/Key.md)

The state of the instance and its fields can be modified arbitrarily if `adminKey` signs a transaction to modify it.
If this is null, then such modifications are not possible, and there is no administrator that can override the normal operation of this smart contract instance.
Note that if it is created with no admin keys, then there is no administrator to authorize changing the admin keys, so there can never be any admin keys for that instance.

---

##### `autoRenewAccountId`: [`AccountId`](../cryptocurrency/AccountId)

ID of the account to charge for auto-renewal of this contract.

---

##### `autoRenewPeriod`: `Duration`

The expiration time will extend every this many seconds.
If there are insufficient funds, then it extends as long as possible.
If the account is empty when it expires, then it is deleted.

---

##### `balance`: [`Hbar`](../Hbar.md)

The current balance, in tinybars.

---

##### `contractAccountId`: `String`

ID of both the contract instance and the cryptocurrency account owned by the contract instance, in the format used by Solidity.

---

##### `contractId`: [`ContractId`](ContractId.md)

ID of the contract instance.

---

##### `contractMemo`: `String`

The memo associated with the contract (max 100 bytes).

---

##### `expirationTime`: `Timestamp`

The current time at which this contract instance (and its account) is set to expire.

---

##### `isDeleted`: `bool`

Whether the contract has been deleted.

---

##### `ledgerId`: [`LedgerId`](../LedgerId.md)

The ID of the ledger which returned this response

---

##### `stakingInfo`: [`StakingInfo`](../StakingInfo.md)

Staking metadata for this contract.

---

##### `storage`: `Uint64`

Number of bytes of storage being used by this instance (which affects the cost to extend the expiration time).

---

##### `tokenRelationships`: `Map` < [`TokenId`](../token/TokenId.md), [`TokenRelationship`](../token/TokenRelationship.md) >

The tokens associated to the contract.
