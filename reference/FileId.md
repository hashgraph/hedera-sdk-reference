# `FileId`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`shard`](#shard) | ✅ | ✅ | O
| [`realm`](#realm) | ✅ | ✅ | O
| [`num`](#num) | ✅ | ✅ | O
| [`constructor()`](#constructor) | ✅ | ✅ | O
| [`fromString()`](#fromstring) | ✅ | ✅ | O
| [`toBytes()`](#tobytes) | ✅ | ✅ | O
| [`fromBytes()`](#frombytes) | ✅ | ✅ | O
| [`equals()`](#equals) | ✅ | ✅ | O
| [`hashCode()`](#hashcode) | ✅ | ✅ | O

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

### `hashCode()`

```typescript
hachCode(): int
```