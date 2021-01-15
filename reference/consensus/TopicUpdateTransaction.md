# `TopicUpdateTransaction`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`TopicId`](#topicid-topicid) | ✅ | ✅ | ✅
| [`TopicMemo`](#topicmemo-string) | ✅ | ✅ | ✅
| [`AdminKey`](#adminkey-key) | ✅ | ✅ | ✅
| [`SubmitKey`](#submitkey-key) | ✅ | ✅ | ✅
| [`AutoRenewPeriod`](#autorenewperiod-duration) | ✅ | ✅ | ✅
| [`AutoRenewAccountId`](#autorenewaccountid-accountid) | ✅ | ✅ | ✅
</details>

> class `TopicUpdateTransaction` extends [`Transaction`](reference/Transaction.md)

<!-- tabs:start -->

#### ** Java **

```java
new TopicUpdateTransaction()
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .setTopicId(TopicId.fromString("0.0.5007"))
    .execute(client)
    .getReceipt(client)
```

#### ** JavaScript **

```js
await(
    await new TopicUpdateTransaction()
        .setNodeAccountIds(Collections.singletonList(response.nodeId))
        .setTopicId(TopicId.fromString("0.0.5007"))
        .execute(client)
).getReceipt(client)
```

#### ** Go **

```go
response, err := hedera.NewTopicUpdateTransaction().
    SetTopicID(topicID).
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetTopicMemo(newTopicMemo).
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

### Methods

### `clearTopicMemo()`

```typescript
clearTopicMemo(): this
```

### `clearAdminKey()`

```typescript
clearAdminKey(): this
```

### `clearSubmitKey()`

```typescript
clearSubmitKey(): this
```

### `clearAutoRenewAccountId()`

```typescript
clearAutoRenewAccountId(): this
```

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
