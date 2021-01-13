# `LiveHashAddTransaction`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`AccountId`](#accountid-accountidreferencecryptocurrencyaccountidmd) | ✅ | ✅ | ✅
| [`Hash`](#hash-bytes) | ✅ | ✅ | ✅
</details>

> class `LiveHashAddTransaction` extends [`Transaction`](reference/Transaction.md)

<!-- tabs:start -->

#### ** Java **

```java
new LiveHashAddTransaction()
    .setTopicId(topicId)
    .execute(client)
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .getReceipt(client);
```

#### ** JavaScript **

```js
await (
    await new LiveHashAddTransaction().setTopicId(topic).execute(client)
).getReceipt(client);
```

#### ** Go **

```go
response, err = NewLiveHashAddTransaction().
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

### Properties

##### `AccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

---

##### `Hash`: `bytes`

---

