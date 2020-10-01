# `ContractFunctionResult`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`contractId`](#contractid) | ✅ | ✅ | O
| [`errorMessage`](#errormessage) | ✅ | ✅ | O
| [`bloom`](#bloom) | ✅ | ✅ | O
| [`gasUsed`](#gasused) | ✅ | ✅ | O
| [`logs`](#logs) | ✅ | ✅ | O
| [`asBytes()`](#asbytes) | ✅ | ✅ | O
| [`getString()`](#getstring) | ✅ | ✅ | O
| [`getStringArray()`](#getstringarray) | ✅ | ✅ | O
| [`getBytes()`](#getbytes) | ✅ | ✅ | O
| [`getBytes32()`](#getbytes32) | ✅ | ✅ | O
| [`getDynamicBytes()`](#getdynamicbytes) | ✅ | ✅ | O
| [`getBool()`](#getbool) | ✅ | ✅ | O
| [`getInt8()`](#getint8) | ✅ | ✅ | O
| [`getInt32()`](#getint32) | ✅ | ✅ | O
| [`getInt64()`](#getint64) | ✅ | ✅ | O
| [`getInt256()`](#getint256) | ✅ | ✅ | O
| [`getUint8()`](#getuint8) | ✅ | ✅ | O
| [`getUint32()`](#getuint32) | ✅ | ✅ | O
| [`getUint64()`](#getuint64) | ✅ | ✅ | O
| [`getUint256()`](#getuint256) | ✅ | ✅ | O
| [`getAddress()`](#getaddress) | ✅ | ✅ | O

## Fields

### `contractId`

```typescript
contractId: ContractId
```

### `errorMessage`

```typescript
errorMessage: string
```

### `bloom`

```typescript
bloom: bytes
```

### `gasUsed`

```typescript
gasUsed: long
```

### `logs`

```typescript
logs: List<ContractLogInfo>
```

## Methods

### `asBytes()`

```typescript
asBytes(): bytes
```

### `getString()`

```typescript
getString(index: int): string
```

### `getStringArray()`

```typescript
getStringArray(index: int): List<string>
```

### `getBytes()`

```typescript
getBytes(index: int): bytes
```

### `getBytes32()`

```typescript
getBytes32(index: int): bytes
```

### `getDynamicBytes()`

```typescript
getDynamicBytes(index: int): bytes
```

### `getBool()`

```typescript
getBool(index: int): boolean
```

### `getInt8()`

```typescript
getInt8(index: int): byte
```

### `getInt32()`

```typescript
getInt32(index: int): int
```

### `getInt64()`

```typescript
getInt64(index: int): long
```

### `getInt256()`

```typescript
getInt256(index: int): BigInteger
```

### `getUint8()`

```typescript
getUint8(index: int): byte
```

### `getUint32()`

```typescript
getUint32(index: int): int
```

### `getUint64()`

```typescript
getUint64(index: int): long
```

### `getUint256()`

```typescript
getUint256(index: int): BigInteger
```

### `getAddress()`

```typescript
getAddress(index: int): string
```