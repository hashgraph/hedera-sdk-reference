# `ContractId`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`shard`](#shard) | ✅ | ✅ | O
| [`realm`](#realm) | ✅ | ✅ | O
| [`num`](#num) | ✅ | ✅ | O
| [`constructor()`](#constructor) | ✅ | ✅ | O
| [`fromString()`](#fromstring) | ✅ | ✅ | O
| [`fromSolidityAddress()`](#fromsolidityaddress) | ✅ | ✅ | O
| [`toSolidityAddress`](#tosolidityaddress) | ✅ | ✅ | O
| [`toBytes()`](#tobytes) | ✅ | ✅ | O
| [`fromBytes()`](#frombytes) | ✅ | ✅ | O
| [`equals()`](#equals) | ✅ | ✅ | O

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