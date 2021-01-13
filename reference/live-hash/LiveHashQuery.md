# class `LiveHashQuery`

Retrieve the latest state of a topic.

This method is unrestricted and allowed on any topic by any payer account.

Deleted accounts will not be returned.

Returns [`LiveHash`](./LiveHash.md) from [`execute`](../Query.md).

## Static Methods

### `constructor()`

Creates an empty transaction, ready for configuration.

## Properties

### `AccountId` : [`AccountId`](reference/cryptocurrency/AccountId.md)

The Account for which information is being requested.

---

### `Hash` : `bytes`

---
## Declaration

```typescript
class LiveHashQuery extends Query<LiveHash> {
    constructor();

    getTopicId(): TopicId;
    setTopicId(topicId: TopicId): this;
}
```
