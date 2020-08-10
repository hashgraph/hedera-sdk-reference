# `FreezeTransaction`

Set the freezing period in which the platform will stop creating events and accepting transactions.

This is used before safely shut down the platform for maintenance.

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor`](#constructor) | ✅ | ✅ | ✅
| [`setStartTime`](#setStartTime) | ✅ | ✅ | ✅
| [`setEndTime`](#setEndTime) | ✅ | ✅ | ✅

## Methods

### `constructor`

```typescript
constructor()
```

### `setStartTime`

Sets the start time (in UTC).

```typescript
setStartTime(hour: Int, minute: Int): this
```

### `setEndTime`

Sets the end time (in UTC).

```typescript
setEndTime(hour: Int, minute: Int): this
```
