# `TransactionRecord`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`receipt`](#receipt) | ✅ | ✅ | O
| [`transactionHash`](#transactionhash) | ✅ | ✅ | O
| [`consensusTimestamp`](#consensustimestamp) | ✅ | ✅ | O
| [`transactionId`](#transactionid) | ✅ | ✅ | O
| [`transactionMemo`](#transactionmemo) | ✅ | ✅ | O
| [`transactionFee`](#transactionfee) | ✅ | ✅ | O
| [`contractFunctionResult`](#contractfunctionresult) | ✅ | ✅ | O
| [`transfers`](#transfers) | ✅ | ✅ | O
| [`fromString()`](#fromstring) | ✅ | ✅ | O
| [`toBytes()`](#tobytes) | ✅ | ✅ | O
| [`fromBytes()`](#frombytes) | ✅ | ✅ | O

## Fields

### `receipt`

```typescript
receipt: TransactionReceipt
```

### `transactionHash`

```typescript
transactionHash: bytes
```

### `consensusTimestamp`

```typescript
consensusTimestamp: Timestamp
```

### `transactionId`

```typescript
transactionId: TransactionId
```

### `transactionMemo`

```typescript
transactionMemo: string
```

### `transactionFee`

```typescript
transactionFee: Hbar
```

### `contractFunctionResult`

```typescript
contractFunctionResult: ContractFunctionResult
```

### `transfers`

```typescript
transfers: List<Transfers>
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