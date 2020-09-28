# `SystemDeleteTransaction`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`setExpirationTime()`](#setexpirationtime) | ✅ | ✅ | ✅
| [`getExpirationTime()`](#getexpirationtime) | ✅ | ✅ | O
| [`setContractId()`](#setcontractid) | ✅ | ✅ | ✅
| [`getContractId()`](#getcontractid) | ✅ | ✅ | O
| [`setFileId()`](#setfileid) | ✅ | ✅ | ✅
| [`getFileId()`](#getfileid) | ✅ | ✅ | O
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

### `constructor()`

```typescript
constructor(body: TransactionBody)
```

### `setExpirationTime()`

```typescript
setExpirationTime(date: Timestamp): this
```

### `getExpirationTime()`

```typescript
getExpirationTime(): Timestamp
```

### `setContractId()`

```typescript
setContractId(id: ContractId): this
```

### `getContractId()`

```typescript
getContractId(): ContractId
```

### `setFileId()`

```typescript
setFileId(id: FileId): this
```

### `getFileId()`

```typescript
getFileId(): FileId
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
signWith(key: PrivateKey, signer: Function<bytes, bytes>): this
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
