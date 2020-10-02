# `AccountCreateTransaction`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`setKey()`](#setkey) | ✅ | ✅ | ✅
| [`getKey()`](#getkey) | ✅ | ✅ | ✅
| [`setAutoRenewPeriod()`](#setautorenewperiod) | ✅ | ✅ | ✅
| [`getAutoRenewPeriod()`](#getautorenewperiod) | ✅ | ✅ | O
| [`setInitialBalance()`](#setinitialbalance) | ✅ | ✅ | ✅
| [`getInitialBalance()`](#getinitialbalance) | ✅ | ✅ | O
| [`setReceiveRecordThreshold()`](#setreceiverecordthreshold) | ✅ | ✅ | ✅
| [`getReceiveRecordThreshold()`](#getreceiverecordthreshold) | ✅ | ✅ | O
| [`setSendRecordThreshold()`](#setsendrecordthreshold) | ✅ | ✅ | ✅
| [`getSendRecordThreshold()`](#getsendrecordthreshold) | ✅ | ✅ | O
| [`setProxyAccountId()`](#setproxyaccountid) | ✅ | ✅ | ✅
| [`getProxyAccountId()`](#getproxyaccountid) | ✅ | ✅ | O
| [`setReceiverSignatureRequired()`](#setreceiversignaturerequired) | ✅ | ✅ | ✅
| [`getReceiverSignatureRequired()`](#getreceiversignaturerequired) | ✅ | ✅ | O
| [`execute()`](#execute) | ✅ | ✅ | O
| [`setNodeId()`](#setnodeid) | ✅ | ✅ | O
| [`getNodeId()`](#getnodeid) | ✅ | ✅ | O
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

### `setKey()`

```typescript
setKey(key: Key): this
```

### `getKey()`

```typescript
getKey(): Key
```

### `setAutoRenewPeriod()`

```typescript
setAutoRenewPeriod(period: Timestamp): this
```

### `getAutoRenewPeriod()`

```typescript
getAutoRenewPeriod(): Timestamp
```

### `setInitialBalance()`

```typescript
setInitialBalance(balance: Hbar): this
```

### `getInitialBalance()`

```typescript
getInitialBalance(): Hbar
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

### `getNodeId()`

```typescript
getNodeId(): AccountId
```

### `setTransactionValidDuration()`

```typescript
setTransactionValidDuration(duration: Timestamp): this
```

### `getTransactionValidDuration()`

```typescript
getTransactionValidDuration(): Timestamp
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
setTransactionMemo(memo: string): this
```

### `getTransactionMemo()`

```typescript
getTransactionMemo(): string
```

### `toBytes()`

```typescript
toBytes(): bytes
```

### `fromBytes()`

```typescript
fromBytes(data: bytes): this
```

### `getTransactionHash()`

```typescript
getTransactionHash(): bytes
```

### `getTransactionId()`

```typescript
getTransactionId(): TransactionId
```

### `setTransactionId()`

```typescript
setTransactionId(id: TransactionId): this
```

### `sign()`

```typescript
sign(key: PrivateKey): this
```

### `signWith()`

```typescript
signWith(key: PublicKey, signer: Function<bytes, bytes>): this
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