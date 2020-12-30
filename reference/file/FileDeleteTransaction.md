# `FileDeleteTransaction`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`setFileId()`](#setfileid)
| [`getFileId()`](#getfileid)
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

### `setFileId()`

```typescript
setFileId(id: FileId): this
```

### `getFileId()`

```typescript
setFileId(): FileId
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
