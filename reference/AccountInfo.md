# `AccountInfo`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`accountId`](#accountid) | ✅ | ✅ | ✅
| [`contractAccountId`](#contractaccountId) | ✅ | ✅ | ✅
| [`isDeleted`](#isdeleted) | ✅ | ✅ | ✅
| [`proxyAccountId`](#proxyaccountId) | ✅ | ✅ | ✅
| [`proxyReceived`](#proxyreceived) | ✅ | ✅ | ✅
| [`key`](#key) | ✅ | ✅ | ✅
| [`balance`](#balance) | ✅ | ✅ | ✅
| [`generateSendRecordThreshold`](#generatesendrecordthreshold) | ✅ | ✅ | ✅
| [`generateReceiveRecordThreshold`](#generatereceiverecordthreshold) | ✅ | ✅ | ✅
| [`isReceiverSignatureRequired`](#isreceiversignaturerequired) | ✅ | ✅ | ✅
| [`expirationTime`](#expirationtime) | ✅ | ✅ | ✅
| [`autoRenewPeriod`](#autorenewperiod) | ✅ | ✅ | ✅
| [`toBytes()`](#tobytes) | ✅ | ✅ | O
| [`fromBytes`](#frombytes) | ✅ | ✅ | O

## Fields

### `accountId`

```typescript
accountId: AccountId
```

### `contractAccountId`

```typescript
contractAccountId: string
```

### `isDeleted`

```typescript
isDeleted: bool
```

### `proxyAccountId`

```typescript
proxyAccountId: AccountId
```

### `proxyReceived`

```typescript
proxyReceived: Hbar
```

### `key`

```typescript
key: Key
```

### `balance`

```typescript
balance: Hbar
```

### `generateSendRecordThreshold`

```typescript
sendRecordThreshold: Hbar
```

### `generateReceiveRecordThreshold`

```typescript
receiveRecordThreshold: Hbar
```

### `isReceiverSignatureRequired`

```typescript
isReceiverSignatureRequired: bool
```

### `expirationTime`

```typescript
expirationTime: Timestamp
```

### `autoRenewPeriod`

```typescript
autoRenewPeriod: Timestamp
```

### `liveHashes`

```typescript
liveHashes: List<LiveHash>
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