# `FileInfo`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`fileId`](#fileid) | ✅ | ✅ | O
| [`size`](#size) | ✅ | ✅ | O
| [`expirationTime`](#expirationtime) | ✅ | ✅ | O
| [`deleted`](#isdeleted) | ✅ | ✅ | O
| [`keys`](#keys) | ✅ | ✅ | O
| [`toBytes()`](#tobytes) | ✅ | ✅ | O
| [`fromBytes`](#frombytes) | ✅ | ✅ | O


## Fields

### `fileid`

```typescript
fileId: FileId
```

### `size`

```typescript
size: long
```

### `expirationTime`

```typescript
expirationTime: Timestamp
```

### `isDeleted`

```typescript
deleted: bool
```

### `keys`

```typescript
keys: List<Key>
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
