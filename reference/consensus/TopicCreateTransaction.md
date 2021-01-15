# `TopicCreateTransaction`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`TopicId`](#topicid-topicidreferenceconsensustopicidmd) | ✅ | ✅ | ✅
| [`TopicMemo`](#topicmemo-string) | ✅ | ✅ | ✅
| [`AdminKey`](#adminkey-keyreferencecryptographykeymd) | ✅ | ✅ | ✅
| [`SubmitKey`](#submitkey-keyreferencecryptographykeymd) | ✅ | ✅ | ✅
| [`AutoRenewPeriod`](#autorenewperiod-duration) | ✅ | ✅ | ✅
| [`AutoRenewAccountId`](#autorenewaccountid-accountidreferencecryptocurrencyaccountidmd) | ✅ | ✅ | ✅
</details>

> class `TopicCreateTransaction` extends [`Transaction`](reference/Transaction.md)

<!-- tabs:start -->

#### ** Java **

```java

var newTopicId = new TopicCreateTransaction()
    .setAdminKey(operatorKey)
    .setTopicMemo("[e2e::TopicCreateTransaction]")
    .execute(client)
    .getReceipt(client)
    .topicId;
```

#### ** JavaScript **

```js

const response = await new TopicCreateTransaction()
    .setAdminKey(operatorKey)
    .setSubmitKey(operatorKey)
    .setAutoRenewAccountId(operatorId)
    .execute(client);

const receipt = await response.getReceipt(client);

const newTopicId = receipt.topicId;
```

#### ** Go **

```go

response, err := hedera.NewTopicCreateTransaction().
    SetAdminKey(client.GetOperatorPublicKey()).
    SetSubmitKey(client.GetOperatorPublicKey()).
    SetTopicMemo(topicMemo).
    Execute(client) // TransactionResponse
if err != nil {
    println(err.Error())
}

receipt, err := response.GetReceipt(client)
if err != nil {
    println(err.Error())
}

topicID := *receipt.TopicID
```

<!-- tabs:end -->

### Constructor

##### `constructor`()

---

### Properties

##### `TopicId`: [`TopicId`](reference/consensus/TopicId.md)

---

##### `AdminKey`: [`Key`](reference/cryptography/Key.md)

---

##### `SubmitKey`: [`Key`](reference/cryptography/Key.md)

---

##### `AutoRenewPeriod`: `Duration`

---

##### `AutoRenewAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

---

##### `TopicMemo`: `String`

---
