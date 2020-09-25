# `ContractCallQuery`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#new) | ✅ | ✅ | ✅
| [`setContractId()`](#setContractId) | ✅ | ✅ | ✅
| [`setFunction()`](#setfunction) | ✅ | ✅ | ✅
| [`setFunctionParameters()`](#setfunctionparameters) | ✅ | ✅ | O
| [`getFunctionParameters()`](#getfunctionparameters) | ✅ | ✅ | O
| [`setMaxResultSize()`](#setMaxResultSize) | ✅ | ✅ | ✅
| [`setGas()`](#setgas) | ✅ | ✅ | ✅
| [`getGas()`](#getgas) | ✅ | ✅ | ✅
| [`execute()`](#execute) | ✅ | ✅ | ✅
| [`setNodeId()`](#setnodeid) | ✅ | ✅ | O
| [`setQueryPayment()`](#setquerypayment) | ✅ | ✅ | O  
| [`setMaxQueryPayment()`](#setmaxquerypayment) | ✅ | ✅ | O
| [`getCost()`](#getcost) | ✅ | ✅ | O
| [`toBytes()`](#tobytes) | ✅ | ✅ | O
| [`fromBytes()`](#frombytes) | ✅ | ✅ | O

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
setFunctionParameters(parameters: byte[]): this
```

### `getFunctionParameters()`

```typescript
getFunctionParameters(): byte[]
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
toBytes(): byte[]
```

### `fromBytes()`

```typescript
fromBytes(bytes: byte[]): this
```
