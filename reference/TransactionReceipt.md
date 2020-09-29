# `TransactionReceipt`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`status`](#status) | ✅ | ✅ | O
| [`exchangeRate`](#exchangerate) | ✅ | ✅ | O
| [`accountId`](#accountid) | ✅ | ✅ | O
| [`fileId`](#fileid) | ✅ | ✅ | O
| [`contractId`](#contractid) | ✅ | ✅ | O
| [`topicId`](#topicid) | ✅ | ✅ | O
| [`topicSequenceNumber`](#topicsequencenumber) | ✅ | ✅ | O
| [`topicRunningsHash`](#topicrunningshash) | ✅ | ✅ | O
| [`fromString()`](#fromstring) | ✅ | ✅ | O
| [`toBytes()`](#tobytes) | ✅ | ✅ | O
| [`fromBytes()`](#frombytes) | ✅ | ✅ | O

## Fields

### `status`

```typescript
status: Status
```

### `exchangeRate`

```typescript
exchangeRate: ExchangeRate
```

### `accountId`

```typescript
accountId: AccountId
```

### `fileId`

```typescript
FileId: FileId
```

### `contractId`

```typescript
contractId: ContractId
```

### `topicId`

```typescript
topicId: TopicId
```

### `topicSequenceNumber`

```typescript
topicSequenceNumber: long
```

### `topicRunningHash`

```typescript
topicRunningHash: bytes
```

## Methods

### `fromString()`

```typescript
generate(string: string): this
````

### `fromBytes()`

```typescript
fromBytes(data: bytes): this
````

### `toBytes()`

```typescript
toBytes(): bytes
````