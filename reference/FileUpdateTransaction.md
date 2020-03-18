# `FileUpdateTransaction`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#new) | ✅ | ✅ | ✅
| [`setFileId()`](#setFileId) | ✅ | ✅ | ✅
| [`setExpirationTime()`](#setExpirationTime) | ✅ | ✅ | ✅
| [`addKey()`](#addKey) | ✅ | ✅ | ✅
| [`setContents()`](#setContents) | ✅ | ✅ | ✅

## Methods

### `constructor()`

```typescript
constructor()
```

### `setFileId()`

```typescript
setFileId(id: FileId): this
```

### `setExpirationTime()`

```typescript
setExpirationTime(date: Time): this
```

### `addKey()`

```typescript
addKey(key: PublicKey): this
```

### `setContents()`

```typescript
setContents(contents: Uint8Array | string): this
```
