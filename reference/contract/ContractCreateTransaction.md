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
setAdminKey(adminKey: Key): this
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
setAutoRenewPeriod(period: Timestamp): this
```

### `getAutoRenewPeriod()`

```typescript
getAutoRenewPeriod(): Timestamp
```

### `setConstructorParams()`

```typescript
setConstructorParameters(
    params: ContractFunctionParams 
    | params: bytes): this
```

### `getConstructorParams()`

```typescript
getConstructorParameters(): bytes
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