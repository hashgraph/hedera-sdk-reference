> class `ContractUpdateTransaction` extends [`Transaction`](reference/core/Transaction.md)

<!-- tabs:start -->

#### ** Java **

```java
new ContractUpdateTransaction()
    .setContractId(contractId)
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .setContractMemo("[e2e::ContractUpdateTransaction]")
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await new ContractUpdateTransaction()
        .setContractId(contract)
        .setNodeAccountIds([response.nodeId])
        .setContractMemo("[e2e::ContractUpdateTransaction]")
        .setMaxTransactionFee(new Hbar(5))
        .execute(client)
).getReceipt(client);
```

#### ** Go **

```go
response, err := hedera.NewContractUpdateTransaction().
    SetContractID(contractID).
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetContractMemo("[e2e::ContractUpdateTransaction]").
    Execute(client)
if err != nil {
    println(err.Error())
}

receipt, err := response.GetReceipt(client)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Constructor

##### `constructor`()

---

### Properties

##### `contractId`: [`ContractId`](reference/contract/ContractId.md)

The id of the contract to be updated.

---

##### `adminKey`: [`Key`](reference/cryptography/Key.md)

The new key to control updates/deletion of the contract.

---

##### `expirationTime`: `Timestamp`

The new expiry of the contract, no earlier than the current expiry.

---

##### `proxyAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

Deprecated: with no replacement

***Not yet implemented***
<br>
The new id of the account to which the contract is proxy staked.

---

##### `autoRenewPeriod`: `Duration`

***Not yet implemented***
<br>
The new interval at which the contract will pay to extend its expiry.

---

##### `bytecodeFileId`: [`FileId`](reference/file/FileId.md)

The new id of the file asserted to contain the bytecode of the Solidity transaction that created this contract.

---

##### `contractMemo`: `String`

The new contract memo, assumed to be Unicode encoded with UTF-8 (at most 100 bytes).

---

##### `stakedNodeAccountId`: `?AccountId`

ID of the account to which this contract is staking.

---

##### `stakedNodeId`: `?Int64`

ID of the node this contract is staked to.

---

##### `declineStakingReward`: `?bool`

If true, the contract declines receiving a staking reward. The default value is false.

---
