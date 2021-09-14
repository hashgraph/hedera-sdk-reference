> class `TopicInfoQuery` extends [`Query`](reference/core/Query.md) < [`TopicInfo`](reference/consensus/TopicInfo.md) >

Retrieve the latest state of a topic.

This method is unrestricted and allowed on any topic by any payer account.

Deleted accounts will not be returned.

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`topicId`](#topicid-topicid) | ✅ | ✅ | ✅

</details>

<!-- tabs:start -->

#### ** Java **

```java
var info = new TopicInfoQuery()
    .setTopicId(topicId)
    .execute(client)
```

#### ** JavaScript **

```javascript
const info = await new TopicInfoQuery({ topicId }).execute(client); // Uint8Array
```

#### ** Go **

```go
info, err := hedera.NewTopicInfoQuery().
    SetTopicID(topicID).
    Execute(client)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Constructor

##### `constructor`()

---

## Properties

### `topicId` : [`TopicId`](reference/consensus/TopicId.md)

This is the topic ID for which info will be queried for.
