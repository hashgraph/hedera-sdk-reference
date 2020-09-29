# `TransactionId`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`accountId`](#accountid) | ✅ | ✅ | O
| [`validStart`](#validstart) | ✅ | ✅ | O
| [`constructor()`](#constructor) | ✅ | ✅ | O
| [`fromString()`](#fromstring) | ✅ | ✅ | O
| [`generate()`](#generate) | ✅ | ✅ | O
| [`toBytes()`](#tobytes) | ✅ | ✅ | O
| [`fromBytes()`](#frombytes) | ✅ | ✅ | O
| [`getReceipt()`](#getreceipt) | ✅ | ✅ | O
| [`getRecord()`](#getrecord) | ✅ | ✅ | O

## Fields

### `accountId`

```typescript
accountId: AccountId
```

### `validStart`

```typescript
validStart: Timestamp
```

### `num`

```typescript
num: long
```

## Methods

### `constructor()`

```typescript
constructor(id: AccountId, validStart: Timestamp)
```

### `fromString()`

```typescript
generate(string: string): this
````

### `generate()`

```typescript
generate(id: AccountId): this
````

### `fromBytes()`

```typescript
fromBytes(data: bytes): this
````

### `toBytes()`

```typescript
toBytes(): bytes
````

### `getReceipt()`

```typescript
async getReceipt(client: Client): TransactionReceipt
````

### `getRecord()`

```typescript
async getRecord(client: Client): TransactionRecord
````