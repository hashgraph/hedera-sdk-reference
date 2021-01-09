# `TopicSubmitTransaction`

<details>
<summary><b>Support</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`TopicId`](#topicid-topicidreferenceconsensustopicidmd) | ✅ | ✅ | ✅
| [`Message`](#message-bytestring) | ✅ | ✅ | ✅
</details>

> class `TopicSubmitTransaction` extends [`Transaction`](reference/Transaction.md)

<!-- tabs:start -->

#### ** Java **

```java
new TopicMessageSubmitTransaction()
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .setTopicId(topicId)
    .setMessage("Hello, from HCS!")
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await new TopicMessageSubmitTransaction()
        .setTopicId(topic)
        .setMessage(contents)
        .execute(client)
).getReceipt(client);
```

#### ** Go **

```go
newKey := hedera.GeneratePrivateKey()

response, err := NewTopicMessageSubmitTransaction().
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetMessage([]byte(Contents)).
    SetTopicID(topicID).
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

### Properties

##### `TopicId`: [`TopicId`](reference/consensus/TopicId.md)

---

##### `Message: `bytes`

---
