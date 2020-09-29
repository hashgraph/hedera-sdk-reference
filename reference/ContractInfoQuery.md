# `ContractInfoQuery`

## Support

| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`setContractId()`](#setcontractid) | ✅ | ✅ | ✅
| [`getContractId()`](#getcontractid) | ✅ | ✅ | O
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