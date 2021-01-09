# `ContractCreateTransaction`

<details>
<summary><b>Support</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`BytecodeFileId`](#bytecodefileid-fileidreferencefilefileidmd) | ✅ | ✅ | ✅
| [`ContractMemo`](#contractmemo-string) | ✅ | ✅ | ✅
| [`AdminKey`](#adminkey-keyreferencecryptographykeymd) | ✅ | ✅ | ✅
| [`Gas`](#gas-uint64) | ✅ | ✅ | ✅
| [`AutoRenewPeriod`](#autorenewperiod-duration) | ✅ | ✅ | ✅
| [`ProxyAccountId`](#proxyaccountid-accountidreferencecryptocurrencyaccountidmd) | ✅ | ✅ | ✅
| [`InitialBalance`](#initialbalance-hbarreferencehbarmd) | ✅ | ✅ | ✅
| [`ConstructorParameters`](#constructorparameters-bytestring) | ✅ | ✅ | ✅
</details>

> class `ContractCreateTransaction` extends [`Transaction`](reference/Transaction.md)

<!-- tabs:start -->

#### ** Java **

```java

var newContractId = new ContractCreateTransaction()
    .setAdminKey(operatorKey)
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .setGas(2000)
    .setConstructorParameters(new ContractFunctionParameters().addString("Hello from Hedera."))
    .setBytecodeFileId(fileId)
    .setContractMemo("[e2e::ContractCreateTransaction]")
    .execute(client)
    .getReceipt(client)
    .topicId;
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
```

- `Duration` is `number` and is the number of seconds

#### ** Go **

```go
response, err := NewContractCreateTransaction().
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

topicId := *receipt.TopicID
```

<!-- tabs:end -->

### Properties

##### `BytecodeFileID`: [`FileId`](reference/file/FileId.md)

---

##### `AdminKey`: [`Key`](reference/cryptography/Key.md)

---

##### `Gas`: `Uint64`

---

##### `InitialBalance`: [`Hbar`](reference/Hbar.md)

---

##### `ProxyAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

---

##### `AutoRenewPeriod`: `Duration`

---

##### `ConstructorParameters`: `bytes`

---

##### `ContractMemo`: `String`

---
