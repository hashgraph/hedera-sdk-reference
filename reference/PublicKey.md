# `PublicKey`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`fromBytes()`](#frombytes) | ✅ | ✅ | O
| [`toBytes()`](#tobytes) | ✅ | ✅ | O
| [`fromString()`](#fromstring) | ✅ | ✅ | O
| [`verify()`](#verify) | ✅ | ✅ | O
| [`equals()`](#equals) | ✅ | ✅ | O

## Methods

### `fromBytes()`

```typescript
fromBytes(data: bytes): this
```

### `toBytes()`

```typescript
toBytes(): bytes
```

### `fromString()`

```typescript
fromString(key: string): this
```

### `toString()`

```typescript
toString(): string
```

### `verify()`

```typescript
verify(message: bytes, signature: bytes): boolean
```

### `equals()`

```typescript
equals(object: Object): boolean
```