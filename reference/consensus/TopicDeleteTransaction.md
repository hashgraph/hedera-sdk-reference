# `TopicDeleteTransaction`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`TopicId`](#topicid) | ✅ | ✅ | ✅
</details>

> class `TopicDeleteTransaction` extends [`Transaction`](reference/Transaction.md)

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

The `TopicId` which should be deleted

---
