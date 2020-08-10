# `AccountUpdateTransaction`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#new) | ✅ | ✅ | ✅
| [`setAccountId()`](#setAccountId) | ✅ | ✅ | ✅
| [`setKey()`](#setKey) | ✅ | ✅ | ✅
| [`setAutoRenewPeriod()`](#setAutoRenewPeriod) | ✅ | ✅ | ✅
| [`setReceiveRecordThreshold()`](#setReceiveRecordThreshold) | ✅ | ✅ | ✅
| [`setSendRecordThreshold()`](#setSendRecordThreshold) | ✅ | ✅ | ✅
| [`setExpirationTime()`](#setExpirationTime) | ✅ | ✅ | ✅
| [`setProxyAccountId()`](#setProxyAccountId) | ✅ | ✅ | ✅
| [`setReceiverSignatureRequired()`](#setReceiverSignatureRequired) | ✅ | ✅ | ✅

## Methods

### `constructor()`

```typescript
constructor()
```

### `setAccountId()`

```typescript
setAccountId(id: AccountId): this
```

### `setKey()`

```typescript
setKey(key: PublicKey): this
```

### `setAutoRenewPeriod()`

```typescript
setAutoRenewPeriod(period: Duration): this
```

### `setReceiveRecordThreshold()`

```typescript
setReceiveRecordThreshold(threshold: Hbar): this
```

### `setSendRecordThreshold()`

```typescript
setSendRecordThreshold(threshold: Hbar): this
```

### `setExpirationTime()`

```typescript
setExpirationTime(date: Time): this
```

### `setProxyAccountId()`

```typescript
setProxyAccountId(id: AccountId): this
```

### `setReceiverSignatureRequired()`

```typescript
setReceiverSignatureRequired(required: bool): this
```
