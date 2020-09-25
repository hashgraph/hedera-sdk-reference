# `ContractCreateTransaction`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`setBytecodeFileId()`](#setbytecodefileid) | ✅ | ✅ | ✅
| [`getBytecodeFileId()`](#getbytecodefileid) | ✅ | ✅ | O
| [`setAdminKey()`](#setadminkey) | ✅ | ✅ | ✅
| [`getAdminKey()`](#getadminkey) | ✅ | ✅ | O
| [`setGas()`](#setgas) | ✅ | ✅ | ✅
| [`getGas()`](#getgas) | ✅ | ✅ | O
| [`setInitialBalance()`](#setinitialbalance) | ✅ | ✅ | ✅
| [`getInitialBalance()`](#getinitialbalance) | ✅ | ✅ | O
| [`setProxyAccountId()`](#setproxyaccountid) | ✅ | ✅ | ✅
| [`getProxyAccountId()`](#getproxyaccountid) | ✅ | ✅ | O
| [`setAutoRenewPeriod()`](#setautorenewperiod) | ✅ | ✅ | ✅
| [`getAutoRenewPeriod()`](#getautorenewperiod) | ✅ | ✅ | O
| [`setConstructorParams()`](#setconstructorparams) | ✅ | ✅ | ✅
| [`getConstructorParams()`](#getconstructorparams) | ✅ | ✅ | ✅
| [`setContractMemo()`](#setcontractmemo) | ✅ | ✅ | ✅
| [`getContractMemo()`](#getcontractmemo) | ✅ | ✅ | ✅
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

### `setBytecodeFileId()`

```typescript
setBytecodeFileId(id: FileId): this
```

### `getBytecodeFileId()`

```typescript
getBytecodeFileId(): FileId
```

### `setAdminKey()`

```typescript
setAdminKey(key: PublicKey): this
```

### `getAdminKey()`

```typescript
getAdminKey(): Key
```

### `setGas()`

```typescript
setGas(gas: long): this
```

### `getGas()`

```typescript
getGas(): long
```

### `setInitialBalance()`

```typescript
setInitialBalance(balance: Hbar): this
```

### `getInitialBalance()`

```typescript
getInitialBalance(): Hbar
```

### `setProxyAccountId()`

```typescript
setProxyAccountId(id: AccountId): this
```

### `getProxyAccountId()`

```typescript
getProxyAccountId(): AccountId
```


### `setAutoRenewPeriod()`

```typescript
setAutoRenewPeriod(period: Duration): this
```

### `getAutoRenewPeriod()`

```typescript
getAutoRenewPeriod(): Duration
```

### `setConstructorParams()`

```typescript
setConstructorParameters(params: ContractFunctionParams): this
```

### `getConstructorParams()`

```typescript
getConstructorParameters(): ByteString
```

### `setContractMemo()`

```typescript
setContractMemo(memo: string): this
```

### `getContractMemo()`

```typescript
getContractMemo(memo: string): string
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