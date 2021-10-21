> class `TopicInfo`

Current state of the topic

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): `TopicInfo`

Deserialize a [`TopicInfo`](#) from its the protobuf representation.

---

### Methods

##### `toBytes` (): `bytes`

Serialize the [`TopicInfo`](#) into its protobuf representation.

---

### Fields

##### `topicId`: [`TopicId`](reference/consensus/TopicId.md)

The ID for which this info belongs to.

---

##### `topicMemo`: `String`

The memo set on the topic.

---

##### `runningHash`: `bytes`

The current running hash of the last topic message.

---

##### `sequenceNumber`: `Uint64`

The sequence number of the last topic message.

---

##### `expirationTime`: `Timestamp`

The timestamp when this topic will expire which will effectively delete this topic.

---

##### `adminKey`: [`Key`](reference/cryptography/Key.md)

The key that is required to sign transactions that mutate this topic.

---

##### `submitKey`: [`Key`](reference/cryptography/Key.md)

The key that is required to sign transactions that submit messages to this topic.

---

##### `autoRenewPeriod`: `Duration`

The duration since topic creation when this topic will be auto renewed and the auto renew account will be charged.

---

##### `autoRenewAccountId`: `AccountId`

The auto renew account that will be charged when the topic is to be auto renewed.

---
