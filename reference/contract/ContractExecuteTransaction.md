# `ContractExecuteTransaction`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`setGas()`](#setgas) | ✅ | ✅ | ✅
| [`getGas()`](#getgas) | ✅ | ✅ | ✅
| [`setPayableAmount()`](#setpayableamount) | ✅ | ✅ | ✅
| [`getPayableAmount()`](#getpayableamount) | ✅ | ✅ | ✅
| [`setFunction()`](#setfunction) | ✅ | ✅ | ✅
| [`setFunctionParameters()`](#setfunctionparameters) | ✅ | ✅ | O
| [`getFunctionParameters()`](#getfunctionparameters) | ✅ | ✅ | O
| [`setContractId()`](#setcontractid) | ✅ | ✅ | ✅
| [`getContractId()`](#getcontractid) | ✅ | ✅ | ✅
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

### `setGas()`

```typescript
setGas(gas: long): this
```

### `getGas()`

```typescript
getGas(): long
```

### `setPayableAmount()`

```typescript
setPayableAmount(payable: Hbar): this
```

### `getPayableAmount()`

```typescript
getPayableAmount(): Hbar
```


### `setFunction()`

```typescript
setFunction(
    name: string
    | name: string, 
    parameters: ContractFunctionParameters): this
```

### `setFunctionParameters()`

```typescript
setFunctionParameters(parameters: bytes): this
```

### `getFunctionParameters()`

```typescript
getFunctionParameters(): bytes
```

### `setContractId()`

```typescript
setContractId(id: ContractId): this
```

### `getContractId()`

```typescript
getContractId(): ContractId
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