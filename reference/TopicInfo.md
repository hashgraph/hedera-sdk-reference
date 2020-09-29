# `TopicInfo`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`topicId`](#topicid) | ✅ | ✅ | O
| [`topicMemo`](#topicid) | ✅ | ✅ | O
| [`runningHash`](#topicid) | ✅ | ✅ | O
| [`sequenceNumber`](#topicid) | ✅ | ✅ | O
| [`expirationTime`](#topicid) | ✅ | ✅ | O
| [`adminKey`](#topicid) | ✅ | ✅ | O
| [`submitKey`](#topicid) | ✅ | ✅ | O
| [`autoRenewPeriod`](#topicid) | ✅ | ✅ | O
| [`autoRenewAccountId`](#topicid) | ✅ | ✅ | O
| [`fromBytes`](#frombytes) | ✅ | ✅ | O


## Fields

### `topicId`

```typescript
topicId: TopicId
```

### `topicMemo`

```typescript
topicMemo: string
```

### `runningHash`

```typescript
runningHash: bytes
```

### `sequenceNumber`

```typescript
sequenceNumber: long
```

### `expirationTime`

```typescript
expirationTime: Timestamp
```

### `adminKey`

```typescript
admingKey: Key
```

### `submitKey`

```typescript
submitKey: Key
```

### `autoRenewPeriod`

```typescript
autoRenewPeriod: Timestamp
```

### `autoRenewAccountId`

```typescript
autoRenewAccountId: AccountId
```

## Methods

### `fromBytes()`

```typescript
fromBytes(data: bytes): this
```

### `toBytes()`

```typescript
toBytes(): bytes
```
