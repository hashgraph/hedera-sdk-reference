# `ConsensusTopicUpdateTransaction`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#new) | ✅ | ✅ | ✅
| [`setTopicId()`](#setTopicId) | ✅ | ✅ | ✅
| [`setTopicMemo()`](#setTopicMemo) | ✅ | ✅ | ✅
| [`setExpirationTime()`](#setExpirationTime) | ✅ | ✅ | ✅
| [`setAdminKey()`](#setAdminKey) | ✅ | ✅ | ✅
| [`setSubmitKey()`](#setSubmitKey) | ✅ | ✅ | ✅
| [`setAutoRenewPeriod()`](#setAutoRenewPeriod) | ✅ | ✅ | ✅
| [`setAutoRenewAccountId()`](#setAutoRenewAccountId) | ✅ | ✅ | ✅
| [`clearTopicMemo()`](#clearTopicMemo) | ✅ | ✅ | ✅
| [`clearAdminKey()`](#clearAdminKey) | ✅ | ✅ | ✅
| [`clearSubmitKey()`](#clearSubmitKey) | ✅ | ✅ | ✅
| [`clearAutoRenewAccountId()`](#clearAutoRenewAccountId) | ✅ | ✅ | ✅

## Methods

### `constructor()`

```typescript
constructor()
```

### `setTopicId()`

```typescript
setTopicId(id: ConsensusTopicId): this
```

### `setTopicMemo()`

```typescript
setTopicMemo(memo: string): this
```

### `setExpirationTime()`

```typescript
setExpirationTime(time: Date): this
```

### `setAdminKey()`

```typescript
setAdminKey(key: PublicKey): this
```

### `setSubmitKey()`

```typescript
setSubmitKey(key: PublicKey): this
```

### `setAutoRenewPeriod()`

```typescript
setAutoRenewPeriod(id: Timestamp): this
```

### `setAutoRenewAccountId()`

```typescript
setAutoRenewAccountId(id: AccountId): this
```

### `clearTopicMemo()`

```typescript
clearTopicMemo(): this
```

### `clearAdminKey()`

```typescript
clearAdminKey(): this
```

### `clearSubmitKey()`

```typescript
clearSubmitKey(): this
```

### `clearAutoRenewAccountId()`

```typescript
clearAutoRenewAccountId(): this
```
