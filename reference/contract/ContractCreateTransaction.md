> class `ContractCreateTransaction` extends [`Transaction`](reference/core/Transaction.md)

<!-- tabs:start -->

#### ** Java **

```java

var contractId = new ContractCreateTransaction()
    .setAdminKey(operatorKey)
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .setGas(2000)
    .setConstructorParameters(new ContractFunctionParameters().addString("Hello from Hedera."))
    .setBytecodeFileId(fileId)
    .setContractMemo("[e2e::ContractCreateTransaction]")
    .execute(client)
    .getReceipt(client)
    .contractId;
```

#### ** JavaScript **

```js
const response = await new ContractCreateTransaction()
    .setAdminKey(operatorKey)
    .setNodeAccountIds([response.nodeId])
    .setGas(2000)
    .setConstructorParameters(
        new ContractFunctionParameters().addString("Hello from Hedera.")
    )
    .setBytecodeFileId(file)
    .setContractMemo("[e2e::ContractCreateTransaction]")
    .setMaxTransactionFee(new Hbar(20))
    .execute(client);

const receipt = await response.getReceipt(client);
const contractId = receipt.contractId;
```

#### ** Go **

```go
response, err := hedera.NewContractCreateTransaction().
    SetAdminKey(client.GetOperatorPublicKey()).
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetGas(2000).
    SetConstructorParameters(NewContractFunctionParameters().AddString("hello from hedera")).
    SetBytecodeFileID(fileID).
    SetContractMemo("hedera-sdk-go::TestContractCreateTransaction_Execute").
    Execute(client)
if err != nil {
    println(err.Error())
}

receipt, err := response.GetReceipt(client)
if err != nil {
    println(err.Error())
}

contractId := *receipt.contractID
```

<!-- tabs:end -->

### Constructor

##### `constructor`()

---

### Properties

##### `bytecodeFileId`: [`FileId`](reference/file/FileId.md)

The `FileId` of the file containing the smart contract byte code.
A copy will be made and held by the contract instance, and have the same expiration time as the instance.

---

##### `adminKey`: [`Key`](reference/cryptography/Key.md)

The state of the instance and its fields can be modified arbitrarily if `adminKey` signs a transaction to modify it.
If this is null, then such modifications are not possible, and there is no administrator that can override the normal operation of this smart contract instance.
Note that if it is created with no admin keys, then there is no administrator to authorize changing the admin keys, so there can never be any admin keys for that instance.

---

##### `gas`: `Uint64`

Gas to run the constructor.

---

##### `initialBalance`: [`Hbar`](reference/Hbar.md)

Initial number of tinybars to put into the cryptocurrency account associated with and owned by the smart contract.

---

##### `proxyAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

Deprecated: with no replacement

`AccountId` of the account to which this account is proxy staked.
If `proxyAccountID` is null, or is an invalid account, or is an account that isn't a node, then this account is automatically proxy staked to a node chosen by the network, but without earning payments.
If the `proxyAccountID` account refuses to accept proxy staking , or if it is not currently running a node, then it will behave as if `proxyAccountID` was null.

---

##### `autoRenewPeriod`: `Duration`

The instance will charge its account every this many seconds to renew for this long.

---

##### `constructorParameters`: `bytes`

Parameters to pass to the constructor.

---

##### `contractMemo`: `String`

The memo that was submitted as part of the contract (max 100 bytes).

---

##### `stakedNodeAccountId`: `?AccountId`

ID of the account to which this contract is staking.

---

##### `stakedNodeId`: `?Int64`

ID of the node this contract is staked to.

---

##### `declineStakingReward`: `bool`

If true, the contract declines receiving a staking reward. The default value is false.

---
