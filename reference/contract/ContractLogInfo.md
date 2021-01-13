# `ContractLogInfo`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`contractId`](#contractid) | ✅ | ✅ | ✅
| [`bloom`](#bloom) | ✅ | ✅ | ✅
| [`topics`](#topics) | ✅ | ✅ | ✅
| [`data`](#data) | ✅ | ✅ | ✅
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`toBytes()`](#tobytes) | ✅ | ✅ | ✅
| [`fromBytes`](#frombytes) | ✅ | ✅ | ✅

</details>

## Fields

### `contractId`

```typescript
contractId: ContractId
```

### `bloom`

```typescript
bloom: bytes
```

### `topics`

```typescript
topics: List<bytes>
```

### `data`

```typescript
data: bytes
```

## Methods

### `constructor()`

```typescript
constructor(
    id: ContractId,
    bloom: bytes,
    topics: List<bytes>,
   data: bytes)
```

### `fromBytes()`

```typescript
fromBytes(data: bytes): this
```

### `toBytes()`

```typescript
toBytes(): bytes
```
