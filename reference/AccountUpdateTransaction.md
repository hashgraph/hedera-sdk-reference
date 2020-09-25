# `AccountUpdateTransaction`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`setAccountId()`](#setaccountdd) | ✅ | ✅ | ✅
| [`getAccountId()`](#getaccountdd) | ✅ | ✅ | ✅
| [`setKey()`](#setkey) | ✅ | ✅ | ✅
| [`getKey()`](#getkey) | ✅ | ✅ | O
| [`setAutoRenewPeriod()`](#setautorenewperiod) | ✅ | ✅ | ✅
| [`getAutoRenewPeriod()`](#getautorenewperiod) | ✅ | ✅ | O
| [`setReceiveRecordThreshold()`](#setreceiverecordthreshold) | ✅ | ✅ | ✅
| [`getReceiveRecordThreshold()`](#getreceiverecordthreshold) | ✅ | ✅ | ✅
| [`setSendRecordThreshold()`](#setsendrecordthreshold) | ✅ | ✅ | ✅
| [`getSendRecordThreshold()`](#getsendrecordthreshold) | ✅ | ✅ | ✅
| [`setExpirationTime()`](#setexpirationtime) | ✅ | ✅ | ✅
| [`getExpirationTime()`](#getexpirationtime) | ✅ | ✅ | O
| [`setProxyAccountId()`](#setproxyaccountId) | ✅ | ✅ | ✅
| [`getProxyAccountId()`](#getproxyaccountid) | ✅ | ✅ | O
| [`setReceiverSignatureRequired()`](#setreceiversignaturerequired) | ✅ | ✅ | ✅
| [`getReceiverSignatureRequired()`](#getreceiversignaturerequired) | ✅ | ✅ | O
| [`execute()`](#execute) | ✅ | ✅ | O
| [`setNodeId()`](#setnodeid) | ✅ | ✅ | O
| [`setTransactionValidDuration()`](#settransactionvalidduration) | ✅ | ✅ | O
| [`getTransactionValidDuration()`](#gettransactionvalidduration) | ✅ | ✅ | O
| [`setMaxTransactionFee()`](#setmaxtransactionfee) | ✅ | ✅ | O
| [`getMaxTransactionFee()`](#getmaxtransactionfee) | ✅ | ✅ | O
| [`setTransactionMemo()`](#settransactionmemo) | ✅ | ✅ | O
| [`getTransactionMemo()`](#gettransactionmemo) | ✅ | ✅ | O
| [`toBytes()`](#tobytes) | ✅ | ✅ | O
| [`fromBytes()`](#frombytes) | ✅ | ✅ | O
| [`getTransactionHash()`](#gettransactionhash) | ✅ | ✅ | O
| [`setTransactionId()`](#settransactionid) | ✅ | ✅ | O
| [`getTransactionId()`](#gettransactionid) | ✅ | ✅ | O
| [`sign()`](#sign) | ✅ | ✅ | O
| [`signWith()`](#signwith) | ✅ | ✅ | O
| [`signWithOperator()`](#signwithoperator) | ✅ | ✅ | O
| [`freeze()`](#freeze) | ✅ |  ✅ | O
| [`freezeWith()`](#freezewith) | ✅ | ✅ | O

## Methods

### `constructor()`

```typescript
constructor()
```

### `setAccountId()`

```typescript
setAccountId(id: AccountId): this
```

### `getAccountId()`

```typescript
getAccountId(): AccountId
```

### `setKey()`

```typescript
setKey(key: PublicKey): this
```

### `getKey()`

```typescript
getKey(): Key
```

### `setAutoRenewPeriod()`

```typescript
setAutoRenewPeriod(period: Duration): this
```

### `getAutoRenewPeriod()`

```typescript
getAutoRenewPeriod(): Duration
```

### `setReceiveRecordThreshold()`

```typescript
setReceiveRecordThreshold(threshold: Hbar): this
```

### `getReceiveRecordThreshold()`

```typescript
getReceiveRecordThreshold(): Hbar
```

### `setSendRecordThreshold()`

```typescript
setSendRecordThreshold(threshold: Hbar): this
```

### `getSendRecordThreshold()`

```typescript
getSendRecordThreshold(): Hbar
```

### `getSendRecordThreshold()`

```typescript
getSendRecordThreshold(): Hbar
```

### `setExpirationTime()`

```typescript
setExpirationTime(date: Timestamp): this
```

### `getExpirationTime()`

```typescript
getExpirationTime(): Timestamp
```

### `setProxyAccountId()`

```typescript
setProxyAccountId(id: AccountId): this
```

### `getProxyAccountId()`

```typescript
getProxyAccountId(): AccountId
```

### `setReceiverSignatureRequired()`

```typescript
setReceiverSignatureRequired(required: bool): this
```

### `getReceiverSignatureRequired()`

```typescript
getReceiverSignatureRequired(): boolean
```

### `execute()`

```typescript
async execute(client: Client): this
```

### `setNodeId()`

```typescript
setNodeId(id: AccountId): this
```

### `setTransactionValidDuration()`

```typescript
setTransactionValidDuration(duration: Duration): this
```

### `getTransactionValidDuration()`

```typescript
getTransactionValidDuration(): Duration
```

### `setMaxTransactionFee()`

```typescript
setMaxTransactionFee(fee: Hbar): this
```

### `getMaxTransactionFee()`

```typescript
getMaxTransactionFee(): Hbar
```

### `setTransactionMemo()`

```typescript
setTransactionMemo(memo: String): this
```

### `getTransactionMemo()`

```typescript
getTransactionMemo(): String
```

### `getTransactionHash()`

```typescript
getTransactionHash(): byte[]
```

### `setTransactionId()`

```typescript
setTransactionId(): TransactionId
```

### `getTransactionId()`

```typescript
getTransactionId(id: TransactionId): this
```

### `sign()`

```typescript
sign(key: PrivateKey): this
```

### `signWith()`

```typescript
signWith(key: PrivateKey, signer: Function<byte[], byte[]>): this
```

### `signWithOperator()`

```typescript
signWithOperator(client: Client): this
```

### `freeze()`

```typescript
freeze(): this
```

### `freezeWith()`

```typescript
freezeWith(client: Client): this
```
