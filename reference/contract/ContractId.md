# `ContractId`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`shard`](#shard) | ✅ | ✅ | ✅
| [`realm`](#realm) | ✅ | ✅ | ✅
| [`num`](#num) | ✅ | ✅ | ✅
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`fromString()`](#fromstring) | ✅ | ✅ | ✅
| [`fromSolidityAddress()`](#fromsolidityaddress) | ✅ | ✅ | ✅
| [`toSolidityAddress`](#tosolidityaddress) | ✅ | ✅ | ✅
| [`toBytes()`](#tobytes) | ✅ | ✅ | ✅
| [`fromBytes()`](#frombytes) | ✅ | ✅ | ✅
| [`equals()`](#equals) | ✅ | ✅ | ✅

## Fields

### `shard`

```typescript
shard: long
```

### `realm`

```typescript
realm: long
```

### `num`

```typescript
num: long
```

## Methods

### `constructor()`

```typescript
constructor(num: long)
```

### `constructor()`

```typescript
constructor(shard: long, realm: long, num: long)
````

### `fromString()`

```typescript
fromString(id: string): this
```

### `fromSolidityAddress()`

```typescript
fromSolidityAddress(address: string): this
```

### `toSolidityAddress()`

```typescript
toSolidityAddress(): string
```

### `fromBytes()`

```typescript
fromBytes(data: bytes): this
```

### `toBytes()`

```typescript
toBytes(): bytes
```

### `equals()`

```typescript
equals(object: Object): boolean
```
