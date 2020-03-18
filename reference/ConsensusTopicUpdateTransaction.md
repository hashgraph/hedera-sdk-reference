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
setTopicMemo(memo: String): this
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
setAutoRenewPeriod(id: Duration): this
```

### `setAutoRenewAccountId()`

```typescript
setAutoRenewAccountId(id: AccountId): this
```

### `clearTopicMemo()`

```typescript
clearTopicMemo(self): this
```

### `clearAdminKey()`

```typescript
clearAdminKey(self): this
```

### `clearSubmitKey()`

```typescript
clearSubmitKey(self): this
```

### `clearAutoRenewAccountId()`

```typescript
clearAutoRenewAccountId(self): this
```

