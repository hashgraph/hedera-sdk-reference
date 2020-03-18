# `ConsensusTopicInfo`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`topicMemo`](#topicMemo) | ✅ | ✅ | ✅
| [`runningHash`](#runningHash) | ✅ | ✅ | ✅
| [`sequenceNumber`](#sequenceNumber) | ✅ | ✅ | ✅
| [`expirationTime`](#expirationTime) | ✅ | ✅ | ✅
| [`adminKey`](#adminKey) | ✅ | ✅ | ✅
| [`submitKey`](#submitKey) | ✅ | ✅ | ✅
| [`autoRenewPeriod`](#autoRenewPeriod) | ✅ | ✅ | ✅
| [`autoRenewAccountId`](#autoRenewAccountId) | ✅ | ✅ | ✅

## Fields

### `topicMemo`

```typescript
topicMemo: string
```

### `runningHash`

```typescript
runningHash: Uint8Array
```

### `sequenceNumber`

```typescript
sequenceNumber: Uint64
```

### `expirationTime`

```typescript
expirationTime: Time
```

### `adminKey`

```typescript
adminKey: Key?
```

### `submitKey`

```typescript
submitKey: Key?
```

### `autoRenewPeriod`

```typescript
autoRenewPeriod: Duration
```

### `autoRenewAccountId`

```typescript
autoRenewAccountId: AccountId?
```
