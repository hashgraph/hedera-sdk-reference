# `LiveHash`

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`accountId`](#accountid) | ✅ | ✅ | ✅
| [`hash`](#hash) | ✅ | ✅ | ✅
| [`keys`](#keys) | ✅ | ✅ | ✅
| [`duration`](#duration) | ✅ | ✅ | ✅
| [`toBytes()`](#tobytes) | ✅ | ✅ | ✅
| [`fromBytes()`](#frombytes) | ✅ | ✅ | ✅

</details>

## Properties

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
