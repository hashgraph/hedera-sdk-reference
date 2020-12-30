# `TopicInfo`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`topicId`](#topicid) | ✅ | ✅ | ✅
| [`topicMemo`](#topicid) | ✅ | ✅ | ✅
| [`runningHash`](#topicid) | ✅ | ✅ | ✅
| [`sequenceNumber`](#topicid) | ✅ | ✅ | ✅
| [`expirationTime`](#topicid) | ✅ | ✅ | ✅
| [`adminKey`](#topicid) | ✅ | ✅ | ✅
| [`submitKey`](#topicid) | ✅ | ✅ | ✅
| [`autoRenewPeriod`](#topicid) | ✅ | ✅ | ✅
| [`autoRenewAccountId`](#topicid) | ✅ | ✅ | ✅
| [`fromBytes`](#frombytes) | ✅ | ✅ | ✅


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
