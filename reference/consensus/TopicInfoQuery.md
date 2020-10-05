# class `TopicInfoQuery`

Retrieve the latest state of a topic.

This method is unrestricted and allowed on any topic by any payer account.

Deleted accounts will not be returned.

Returns [`TopicInfo`](./TopicInfo.md) from [`execute`](../Query.md).

## Static Methods

### `constructor()`

Creates an empty transaction, ready for configuration.

## Properties

### `topicId: TopicId`

The Topic for which information is being requested.

## Declaration

```typescript
class TopicInfoQuery extends Query<TopicInfo> {
    constructor();

    getTopicId(): TopicId;
    setTopicId(topicId: TopicId): this;
}
```
