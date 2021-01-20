> class `TopicMessage`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`consensusTimestamp`](#consensustimestamp-timestamp) | ✅ | ✅ | ✅
| [`contents`](#contents-bytes) | ✅ | ✅ | ✅
| [`runningHash`](#runninghash-bytes) | ✅ | ✅ | ✅
| [`sequenceNumber`](#sequencenumber-uint64) | ✅ | ✅ | ✅
| [`chunks`](#chunks-topicmessagechunk) | ✅ | ✅ | ✅

</details>

<!-- tabs:start -->

#### ** Java **

```java
var handle = new TopicMessageQuery()
    .setTopicId(topicId)
    .setStartTime(Instant.EPOCH)
    .setErrorHandler((e /* Throwable */, message /* TopicMessage */) -> {
        System.err.println(e.getMessage());

        if (message != null) {
            System.err.println("Caused by message: " + new String(message.contents, StandardCharsets.UTF_8));
        }
    })
    .subscribe(client, (message /* TopicMessage */) -> {
        System.out.println(new String(message.contents, StandardCharsets.UTF_8));
    });
```

#### ** JavaScript **

```javascript
const handle = new TopicMessageQuery({ topicId, startTime: 0 })
    .setErrorHandler((error /* error */, message /* TopicMessage */) => {
        console.err(error);

        if (message != null) {
            console.err(`Caused by message: ${utf8.decode(message.contents)}`);
        }
    })
    .subscribe(client, (message /* TopicMessage */) => {
        console.log(utf8.decode(message.contents));
    });
```

#### ** Go **

```go
handle := hedera.NewTopicMessageQuery().
    SetTopicID(topicID).
    SetStartTime(0).
    SetErrorHandler(func(err /* error */) {
        panic(err)
    })
    Subscribe(client, func(message /* TopicMessage */) {
        println(string(message.contents))
    })
```

<!-- tabs:end -->

### Properties

#### `consensusTimestamp`: `Timestamp`

The consensus timestamp of this topic message. If this message was chunked, this
field would be equal to the last chunk's consensus timestamp.

---

#### `contents`: `bytes`

The contents of this topic message. If this message was chunked, this field would
be equal to the concatination of all the chunks.

---

#### `runningHash`: `bytes`

The running hash of this topic message. If this message was chunked this field would
be equal to the last chunk's running hash.

---

#### `sequenceNumber`: `Uint64`

The sequence number of this topic message. If this message was chunked this field would
be equal to the last chunk's sequence number.

---

#### `chunks`: [`TopicMessageChunk[]`](reference/consensus/TopicMessageChunk.md)

The chunks of this topic message. Will be null if this topic message was not chunked.
Otherwise will contain an ordered list of chunks for this topic message.

---
