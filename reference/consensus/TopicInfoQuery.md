# class `TopicInfoQuery`

Retrieve the latest state of a topic.

This method is unrestricted and allowed on any topic by any payer account.

Deleted accounts will not be returned.

Returns [`TopicInfo`](./TopicInfo.md) from [`execute`](../Query.md).

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

The Topic for which information is being requested.

## Declaration

```typescript
class TopicInfoQuery extends Query<TopicInfo> {
    constructor();

    getTopicId(): TopicId;
    setTopicId(topicId: TopicId): this;
}
```
