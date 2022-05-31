> class `StakingInfo`

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): `StakingInfo`

Deserialize a [`StakingInfo`](#) from its the protobuf representation.

---

### Methods

##### `toBytes` (): `bytes`

Serialize the [`StakingInfo`](#) into its protobuf representation.

---

### Properties

##### `declineStakingReward`: `bool`

If true, this account or contract declined to receive a staking reward.

---

##### `stakePeriodStart`: `Timestamp`

The staking period during which either the staking settings for this account or contract changed (such as starting
staking or changing staked\_node\_id) or the most recent reward was earned, whichever is later. If this account or contract
is not currently staked to a node, then this field is not set.

---

###### `pendingReward`: `Int64`

The amount in tinybars that will be received in the next reward situation.

---

###### `stakedToMe`: [`Hbar`](reference/Hbar.md)

The total of balance of all accounts staked to this account or contract.

---

###### `stakedAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The account to which this account or contract is staking.

---

###### `stakedNodeId`: `Uint64`

The ID of the node this account or contract is staked to.

---
