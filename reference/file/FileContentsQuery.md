# `FileContentsQuery`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`setFileId()`](#setfileid) | ✅ | ✅ | ✅
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

### `setFileId()`

```typescript
setFileId(id: FileId): this
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
