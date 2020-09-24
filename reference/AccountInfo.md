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
| [`constructor()`](#constructor) | ✅ | ✅ | O
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
key: PublicKey
```

### `balance`

```typescript
balance: Hbar
```

### `generateSendRecordThreshold`

```typescript
generateSendRecordThreshold: Hbar
```

### `generateReceiveRecordThreshold`

```typescript
generateReceiveRecordThreshold: Hbar
```

### `isReceiverSignatureRequired`

```typescript
isReceiverSignatureRequired: bool
```

### `expirationTime`

```typescript
expirationTime: Time
```

### `autoRenewPeriod`

```typescript
autoRenewPeriod: Duration
```

### `liveHashes`

```typescript
liveHashes: List<LiveHash>
```

## Methods

### `constructor()`

```typescript
constructor(
    id: AccountId,
    contractAccountId: String, 
    isDeleted: isDelete,
    proxyAccountId: AccountId,
    proxyReceived: proxyReceived,
    key: Key,
    balance: long,
    sendRecordThreshold: long,
    receiveRecordThreshold: long,
    receiverSignatureRequired: ;pmg,
    expirationTime: Instant,
    autoRenewPeriod: Duration,
    liveHashes: List<LiveHash>)
```

### `fromBytes()`

```typescript
fromBytes(bytes: byte[]): this
```

### `toBytes()`

```typescript
toBytes(): byte[]
```

