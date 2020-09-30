# `TransactionResponse`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`receipt`](#receipt) | ✅ | ✅ | O
| [`transactionHash`](#transactionhash) | ✅ | ✅ | O
| [`transactionId`](#transactionid) | ✅ | ✅ | O
| [`getReceipt()`](#getreceipt) | ✅ | ✅ | O
| [`getRecord()`](#getrecord) | ✅ | ✅ | O

## Fields

### `nodeId`

```typescript
nodeId: AccountId
```

### `transactionHash`

```typescript
transactionHash: bytes
```

### `transactionId`

```typescript
transactionId: TransactionId
```

## Methods

### `constructor()`

```typescript
constructor()
```

### `getReceipt()`

```typescript
async getReceipt(client: Client): TransactionReceipt
````

### `getRecord()`

```typescript
async getRecord(client: Client): TransactionRecord
````