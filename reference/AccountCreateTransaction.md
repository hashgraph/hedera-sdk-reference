# `AccountCreateTransaction`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#new) | ✅ | ✅ | ✅
| [`setKey()`](#setKey) | ✅ | ✅ | ✅
| [`setAutoRenewPeriod()`](#setAutoRenewPeriod) | ✅ | ✅ | ✅
| [`setInitialBalance()`](#setInitialBalance) | ✅ | ✅ | ✅
| [`setReceiveRecordThreshold()`](#setReceiveRecordThreshold) | ✅ | ✅ | ✅
| [`setSendRecordThreshold()`](#setSendRecordThreshold) | ✅ | ✅ | ✅
| [`setProxyAccountId()`](#setProxyAccountId) | ✅ | ✅ | ✅
| [`setReceiverSignatureRequired()`](#setReceiverSignatureRequired) | ✅ | ✅ | ✅

## Methods

### `constructor()`

```typescript
constructor()
```

### `setKey()`

```typescript
setKey(key: PublicKey): this
```

### `setAutoRenewPeriod()`

```typescript
setAutoRenewPeriod(period: Duration): this
```

### `setInitialBalance()`

```typescript
setInitialBalance(balance: Hbar): this
```

### `setReceiveRecordThreshold()`

```typescript
setReceiveRecordThreshold(threshold: Hbar): this
```

### `setSendRecordThreshold()`

```typescript
setSendRecordThreshold(threshold: Hbar): this
```

### `setProxyAccountId()`

```typescript
setProxyAccountId(id: AccountId): this
```

### `setReceiverSignatureRequired()`

```typescript
setReceiverSignatureRequired(required: bool): this
```

