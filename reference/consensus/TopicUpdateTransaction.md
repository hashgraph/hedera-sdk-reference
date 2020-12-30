# `TopicUpdateTransaction`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`setTopicId()`](#settopicid) | ✅ | ✅ | ✅
| [`getTopicId()`](#gettopicid) | ✅ | ✅ | ✅
| [`setTopicMemo()`](#settopicmemo) | ✅ | ✅ | ✅
| [`getTopicMemo()`](#gettopicmemo) | ✅ | ✅ | ✅
| [`setAdminKey()`](#setadminkey) | ✅ | ✅ | ✅
| [`getAdminKey()`](#getadminkey) | ✅ | ✅ | ✅
| [`setSubmitKey()`](#setsubmitkey) | ✅ | ✅ | ✅
| [`getSubmitKey()`](#getsubmitkey) | ✅ | ✅ | ✅
| [`setAutoRenewPeriod()`](#setautorenewperiod) | ✅ | ✅ | ✅
| [`getAutoRenewPeriod()`](#getautorenewperiod) | ✅ | ✅ | ✅
| [`setAutoRenewAccountId()`](#setautorenewaccountid) | ✅ | ✅ | ✅
| [`getAutoRenewAccountId()`](#getautorenewaccountid) | ✅ | ✅ | ✅
| [`clearTopicMemo()`](#clearyopicmemo) | ✅ | ✅ | ✅
| [`clearAdminKey()`](#clearadminkey) | ✅ | ✅ | ✅
| [`clearSubmitKey()`](#cleardubmitkey) | ✅ | ✅ | ✅
| [`clearAutoRenewAccountId()`](#clearsutotenewsccountid) | ✅ | ✅ | ✅
| [`execute()`](#execute) | ✅ | ✅ | ✅
| [`setNodeId()`](#setnodeid) | ✅ | ✅ | ✅
| [`getNodeId()`](#getnodeid) | ✅ | ✅ | ✅
| [`setTransactionValidDuration()`](#settransactionvalidduration) | ✅ | ✅ | ✅
| [`getTransactionValidDuration()`](#gettransactionvalidduration) | ✅ | ✅ | ✅
| [`setMaxTransactionFee()`](#setmaxtransactionfee) | ✅ | ✅ | ✅
| [`getMaxTransactionFee()`](#getmaxtransactionfee) | ✅ | ✅ | ✅
| [`setTransactionMemo()`](#settransactionmemo) | ✅ | ✅ | ✅
| [`getTransactionMemo()`](#gettransactionmemo) | ✅ | ✅ | ✅
| [`toBytes()`](#tobytes) | ✅ | ✅ | ✅
| [`fromBytes()`](#frombytes) | ✅ | ✅ | ✅
| [`getTransactionHash()`](#gettransactionhash) | ✅ | ✅ | ✅
| [`setTransactionId()`](#settransactionid) | ✅ | ✅ | ✅
| [`getTransactionId()`](#gettransactionid) | ✅ | ✅ | ✅
| [`sign()`](#sign) | ✅ | ✅ | ✅
| [`signWith()`](#signwith) | ✅ | ✅ | ✅
| [`signWithOperator()`](#signwithoperator) | ✅ | ✅ | ✅
| [`freeze()`](#freeze) | ✅ |  ✅ | ✅
| [`freezeWith()`](#freezewith) | ✅ | ✅ | ✅
| [`getSignatures()`](#getsignatures) | ✅ | ✅ | ✅
| [`addSignature()`](#addsignature) | ✅ | ✅ | ✅
| [`getTransactionHashPerNode`](#gettransactionhashpernode) | ✅ | ✅ | ✅
| [`setMaxRetry`](#setmaxretry) | ✅ | ✅ | ✅
| [`getMaxRetry`](#getmaxretry) | ✅ | ✅ | ✅

## Methods

### `constructor()`

```typescript
constructor()
```

### `setTopicId()`

```typescript
setTopicId(id: TopicId): this
```

### `sgtTopicId()`

```typescript
getTopicId(): TopicId
```

### `setTopicMemo()`

```typescript
setTopicMemo(memo: string): this
```

### `getTopicMemo()`

```typescript
getTopicMemo(): string
```

### `setAdminKey()`

```typescript
setAdminKey(key: Key): this
```

### `getAdminKey()`

```typescript
getAdminKey(): Key
```

### `setSubmitKey()`

```typescript
setSubmitKey(key: Key): this
```

### `getSubmitKey()`

```typescript
getSubmitKey(): Key
```

### `setAutoRenewPeriod()`

```typescript
setAutoRenewPeriod(id: Timestamp): this
```

### `getAutoRenewPeriod()`

```typescript
getAutoRenewPeriod(): Timestamp
```

### `setAutoRenewAccountId()`

```typescript
setAutoRenewAccountId(id: AccountId): this
```

### `getAutoRenewAccountId()`

```typescript
getAutoRenewAccountId(): AccountId
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

### `getSignatures()`

```typescript
getSignatures(): Map<AccoundID, Map<PublicKey, byte[]>>
```

### `addSignature()`

```typescript
getSignatures(key: PublicKey, signature: byte[]): this
```

### `getTransactionHashPerNode()`

```typescript
getTransactionHashPerNode(): Map<AccoundID, byte[]>
```

### `setMaxRetry()`

```typescript
setMaxRetry(count: int): this
```

### `getMaxRetry()`

```typescript
getMaxRetry(): int
```
