# `ContractCallQuery`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#new) | ✅ | ✅ | ✅
| [`setContractId()`](#setContractId) | ✅ | ✅ | ✅
| [`setFunction()`](#setFunction) | ✅ | ✅ | ✅
| [`setMaxResultSize()`](#setMaxResultSize) | ✅ | ✅ | ✅
| [`setGas()`](#setGas) | ✅ | ✅ | ✅
| [`execute()`](#execute) | ✅ | ✅ | ✅
| [`getCost()`](#getCost) | ✅ | ✅ | ✅

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
setFunction(name: string, params: ContractFunctionParams): this
```

### `setMaxResultSize()`

```typescript
setMaxResultSize(size: Uint64): this
```

### `setGas()`

```typescript
setGas(size: Uint64): this
```

### `execute()`

```typescript
execute(client: Client): ContractFunctionResult
```

### `getCost()`

```typescript
getCost(client: Client): Hbar
```
