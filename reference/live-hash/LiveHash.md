# `LiveHash`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`accountId`](#accountid) | ✅ | ✅ | ✅
| [`hash`](#hash) | ✅ | ✅ | ✅
| [`keys`](#keys) | ✅ | ✅ | ✅
| [`duration`](#duration) | ✅ | ✅ | ✅
| [`toBytes()`](#tobytes) | ✅ | ✅ | O
| [`fromBytes()`](#frombytes) | ✅ | ✅ | O

## Fields

### `accountId`

```typescript
accountId: AccountId
```

### `hash`

```typescript
hash: bytes
```

### `keys`

```typescript
keys: KeyList
```

### `duration`

```typescript
duration: Timestamp
```

## Methods

### `fromBytes()`

```typescript
fromBytes(data: bytes): this
```

### `toBytes()`

```typescript
toBytes(): bytes
```