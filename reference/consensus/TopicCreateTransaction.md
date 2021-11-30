> class `TopicCreateTransaction` extends [`Transaction`](reference/core/Transaction.md)

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

##### `adminKey`: [`Key`](reference/cryptography/Key.md)

Access control for updating/deleting.
If no adminKey is specified, updateTopic may only be used to extend the topic's `expirationTime`, and deletion
is disallowed.

---

##### `submitKey`: [`Key`](reference/cryptography/Key.md)

Access control for submitMessage. If unspecified, no access control is performed (all submissions are allowed).

---

##### `autoRenewPeriod`: `Duration`

The initial lifetime of the topic and the amount of time to attempt to extend the topic's lifetime by
automatically at the topic's `expirationTime`, if the `autoRenewAccountId` is configured

---

##### `autoRenewAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

Optional account to be used at the topic's `expirationTime` to extend the life of the topic.
The topic lifetime will be extended up to a maximum of the `autoRenewPeriod` or however long the topic
can be extended using all funds on the account.
If specified, there must be an `adminKey` and the `autoRenewAccount` must sign this transaction.

---

##### `topicMemo`: `String`

Short publicly visible memo about the topic. No guarantee of uniqueness.

---
