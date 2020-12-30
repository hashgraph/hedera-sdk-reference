# `ContractCallQuery`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`setContractId()`](#setContractId) | ✅ | ✅ | ✅
| [`setFunction()`](#setfunction) | ✅ | ✅ | ✅
| [`setFunctionParameters()`](#setfunctionparameters) | ✅ | ✅ | ✅
| [`getFunctionParameters()`](#getfunctionparameters) | ✅ | ✅ | ✅
| [`setMaxResultSize()`](#setMaxResultSize) | ✅ | ✅ | ✅
| [`setGas()`](#setgas) | ✅ | ✅ | ✅
| [`getGas()`](#getgas) | ✅ | ✅ | ✅
| [`execute()`](#execute) | ✅ | ✅ | ✅
| [`setNodeId()`](#setnodeid) | ✅ | ✅ | ✅
| [`getNodeId()`](#getnodeid) | ✅ | ✅ | ✅
| [`setQueryPayment()`](#setquerypayment) | ✅ | ✅ | ✅
| [`setMaxQueryPayment()`](#setmaxquerypayment) | ✅ | ✅ | ✅
| [`getCost()`](#getcost) | ✅ | ✅ | ✅
| [`toBytes()`](#tobytes) | ✅ | ✅ | ✅
| [`fromBytes()`](#frombytes) | ✅ | ✅ | ✅

## Methods

### `constructor()`

```typescript
constructor()
```

### `setContractId()`

```typescript
setContractId(id: ContractId): this
```

### `setFunction()`

```typescript
setFunction(name: string): this
```

### `setFunction()`

```typescript
setFunction(name: string, parameters: ContractFunctionParameters): this
```

### `setFunctionParameters()`

```typescript
setFunctionParameters(parameters: bytes): this
```

### `getFunctionParameters()`

```typescript
getFunctionParameters(): bytes
```

### `setMaxResultSize()`

```typescript
setMaxResultSize(size: Uint64): this
```

### `setGas()`

```typescript
setGas(gas: long): this
```

### `getGas()`

```typescript
getGas(): long
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

### `setQueryPayment()`

```typescript
setQueryPayment(payment: Hbar): this
```

### `setMaxQueryPayment()`

```typescript
setMaxQueryPayment(payment: Hbar): this
```

### `getCost()`

```typescript
async getCost(client: Client): Hbar
```

### `toBytes()`

```typescript
toBytes(): bytes
```

### `fromBytes()`

```typescript
fromBytes(data: bytes): this
```
