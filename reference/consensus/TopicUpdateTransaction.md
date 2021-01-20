> class `TopicUpdateTransaction` extends [`Transaction`](reference/core/Transaction.md)

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`topicId`](#topicid-topicid) | ✅ | ✅ | ✅
| [`adminKey`](#adminkey-key) | ✅ | ✅ | ✅
| [`submitKey`](#submitkey-key) | ✅ | ✅ | ✅
| [`autoRenewPeriod`](#autorenewperiod-duration) | ✅ | ✅ | ✅
| [`autoRenewAccountId`](#autorenewaccountid-accountid) | ✅ | ✅ | ✅
| [`topicMemo`](#topicmemo-string) | ✅ | ✅ | ✅
</details>

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

##### `constructor` ()

---

### Methods

##### `clearTopicMemo` ()

Clear the memo for this topic.

---

##### `clearAdminKey` ()

Clear the admin key.
Note: Clearing the admin key will make the topic immutable.

---

##### `clearSubmitKey` ()

Clear the submit key.

---

##### `clearAutoRenewAccountId` ()

Clear the auto renew account ID.

---

### Properties

##### `topicId`: [`TopicId`](reference/consensus/TopicId.md)

`TopicId` to be updated.

---

##### `adminKey`: [`Key`](reference/cryptography/Key.md)

Access control for update/delete of the topic.
If unspecified, no change.
If empty `keyList` - the `adminKey` is cleared.

---

##### `submitKey`: [`Key`](reference/cryptography/Key.md)

Access control for `submitMessage`.
If unspecified, no change.
If empty `keyList` - the `submitKey` is cleared.

---

##### `autoRenewPeriod`: `Duration`

The amount of time to extend the topic's lifetime automatically at `expirationTime` if the `autoRenewAccountId` is
configured and has funds.

---

##### `autoRenewAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

Optional account to be used at the topic's `expirationTime` to extend the life of the topic.
If specified as the default value (0.0.0), the `autoRenewAccountId` will be removed.
If unspecified, no change.

---

##### `topicMemo`: `String`

Short publicly visible memo about the topic. No guarantee of uniqueness. Null for "do not update".

---
