# `LiveHashAddTransaction`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`setAccountId()`](#setaccountid) | ✅ | ✅ | ✅
| [`getAccountId()`](#getaccountid) | ✅ | ✅ | ✅
| [`setHash()`](#sethash) | ✅ | ✅ | ✅
| [`getHash()`](#gethash) | ✅ | ✅ | ✅
| [`setKeys()`](#setkeys) | ✅ | ✅ | ✅
| [`getKeys()`](#getkeys) | ✅ | ✅ | ✅
| [`setDuration()`](#setduration) | ✅ | ✅ | ✅
| [`getDuration()`](#getduration) | ✅ | ✅ | ✅
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

### `constrcutor()`

```typescript
constructor()
```

### `getAccountId()`

```typescript
getAccountId(): AccountId
```

### `setAccountId()`

```typescript
setAccountId(id: AccountId): this
```

### `setHash()`

```typescript
setHash(hash: bytes): this
```

### `getHash()`

```typescript
getHash(): bytes
```

### `setKeys()`

```typescript
setKeys(keys: Key): this
```

### `getKeys()`

```typescript
getKeys(): Collection<Key>
```

### `setDuration()`

```typescript
setDuration(duration: Timestamp): this
```

### `getDuration()`

```typescript
getDuration(): Timestamp
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
