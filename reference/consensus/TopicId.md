# `TopicId`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`shard`](#shard) | ✅ | ✅ | ✅
| [`realm`](#realm) | ✅ | ✅ | ✅
| [`num`](#num) | ✅ | ✅ | ✅
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`fromString()`](#fromstring) | ✅ | ✅ | ✅
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
fromString(id: String): this
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
