# `FileInfo`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`fileId`](#fileid) | ✅ | ✅ | ✅
| [`size`](#size) | ✅ | ✅ | ✅
| [`expirationTime`](#expirationtime) | ✅ | ✅ | ✅
| [`deleted`](#isdeleted) | ✅ | ✅ | ✅
| [`keys`](#keys) | ✅ | ✅ | ✅
| [`toBytes()`](#tobytes) | ✅ | ✅ | ✅
| [`fromBytes()`](#frombytes) | ✅ | ✅ | ✅


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
