# `TopicDeleteTransaction`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`topicId`](#topicid-topicid) | ✅ | ✅ | ✅
</details>

> class `TopicDeleteTransaction` extends [`Transaction`](reference/core/Transaction.md)

<!-- tabs:start -->

#### ** Java **

```java
new TopicDeleteTransaction()
    .setTopicId(topicId)
    .execute(client)
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await new TopicDeleteTransaction().setTopicId(topic).execute(client)
).getReceipt(client);
```

#### ** Go **

```go
response, err = hedera.NewTopicDeleteTransaction().
    SetTopicID(topicID).
    SetNodeAccountIDs([]AccountID{response.NodeID}).
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

##### `topicId`: [`TopicId`](reference/consensus/TopicId.md)

The `topicId` which should be deleted

---
