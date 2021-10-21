> class `TopicMessageQuery`

<!-- tabs:start -->

#### ** Java **

```java
var handle = new TopicMessageQuery()
    .setTopicId(topicId)
    .setStartTime(Instant.EPOCH)
    .subscribe(client, (message) -> {
        receivedMessage[0] = new String(message.contents, StandardCharsets.UTF_8).equals("Hello, from HCS!");
    });
```

#### ** JavaScript **

```javascript
const handle = new TopicMessageQuery()
    .setTopicId(topic)
    .setStartTime(0)
    .subscribe(client, (message) => {
        received = utf8.decode(message.contents) === contents;
    });
```

#### ** Go **

```go
handle, err = hedera.NewTopicMessageQuery().
    SetTopicID(topicID).
    SetStartTime(time.Unix(0, 0)).
    Subscribe(client, func(message TopicMessage) {
        if string(message.Contents) == bigContents {
            wait = false
        }
	})
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

The ID for a topic to subscribe to.

---
