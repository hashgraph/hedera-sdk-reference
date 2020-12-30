# `LiveHashQuery`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`setAccountId()`](#setaccountid) | ✅ | ✅ | ✅
| [`setHash()`](#sethash) | ✅ | ✅ | ✅
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

### `setAccountId()`

```typescript
setAccountId(id: AccountId): this
```

### `setHash()`

```typescript
setHash(hash: bytes): this
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
