> class `ContractCreateFlow`

A helper class to create a contract file bytecode directly. This will use
`FileCreateTransaction` and `FileAppendTransaction` as necessary to create the file
followed by `ContractCreateTransaction` to create the contract, and finally
`FileDeleteTransaction` to delete the created file since it's no longer necessary.

<!-- tabs:start -->

#### ** Java **

```java

var contractId = new ContractCreateFlow()
    .setAdminKey(operatorKey)
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .setGas(2000)
    .setConstructorParameters(new ContractFunctionParameters().addString("Hello from Hedera."))
    .setBytecode(bytecode)
    .setContractMemo("[e2e::ContractCreateFlow]")
    .execute(client)
    .getReceipt(client)
    .contractId;
```

#### ** JavaScript **

```javascript
const response = await new ContractCreateFlow()
    .setAdminKey(operatorKey)
    .setNodeAccountIds([response.nodeId])
    .setGas(2000)
    .setConstructorParameters(
        new ContractFunctionParameters().addString("Hello from Hedera.")
    )
    .setBytecode(bytecode)
    .setContractMemo("[e2e::ContractCreateFlow]")
    .execute(client);

const receipt = await response.getReceipt(client);
const contractId = receipt.contractId;
```

#### ** Go **

```go
response, err := hedera.NewContractCreateFlow().
    SetAdminKey(client.GetOperatorPublicKey()).
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetGas(2000).
    SetConstructorParameters(NewContractFunctionParameters().AddString("hello from hedera")).
    SetBytecode(bytecode).
    SetContractMemo("hedera-sdk-go::TestContractCreateFlow_Execute").
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

##### `bytecode`: `string`

The bytecode for the contract

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
