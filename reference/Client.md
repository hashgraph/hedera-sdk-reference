# `Client`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`setMirrorNetwork()`](#setmirrornetwork) | ✅ | ✅ | O
| [`forNetwork()`](#fornetwork) | ✅ | ✅ | O
| [`forMainnet()`](#formainnet) | ✅ | ✅ | O
| [`forTestnet()`](#fortestnet) | ✅ | ✅ | O
| [`forPreviewnet()`](#forpreviewnet) | ✅ | ✅ | O
| [`fromJson()`](#fromjson) | ✅ | ✅ | O
| [`fromJsonFile()`](#fromjsonfile) | ✅ | ✅ | O
| [`setNetwork()`](#setnetwork) | ✅ | ✅ | O
| [`setOperator()`](#setoperator) | ✅ | ✅ | O
| [`setOperatorWith()`](#setoperatorwith) | ✅ | ✅ | O
| [`getOperatorId()`](#getoperatorid) | ✅ | ✅ | O
| [`getOperatorKey()`](#getoperatorkey) | ✅ | ✅ | O
| [`setMaxTransactionFee()`](#setmaxtransactionfee) | ✅ | ✅ | O
| [`setMaxQueryPayment()`](#setmaxquerypayment) | ✅ | ✅ | O
| [`close()`](#close) | ✅ | X | O

## Methods

### `setMirrorNetwork()`

```typescript
setMirrorNetwork(mirror: List<string>)
```

### `forNetwork()`

```typescript
forNetwork(network: Map<AccountId, String>): this
```

### `forMainnet()`

```typescript
forMainnet(): this
```

### `forTestnet()`

```typescript
forTestnet(): this
```

### `forPreviewnet()`

```typescript
forPreviewnet(): this
```

### `fromJson()`

```typescript
fromJson(json: string): this
```

### `fromJson()`

```typescript
fromJson(json: Reader): this
```

### `fromJsonFile()`

```typescript
fromJsonFile(file: string): this
```

### `fromJsonFile()`

```typescript
fromJsonFile(file: File): this
```

### `setNetwork()`

```typescript
fromJsonFile(nodes: Map<AccountId, String>): this
```

### `setOperator()`

```typescript
setOperator(id: AccountId, key: PrivateKey): this
```

### `setOperatorWith()`

```typescript
setOperatorWith(
    id: AccountId, 
    key: PublicKey, 
    signer: Function<bytes, bytes>): this
```

### `getOperatorId()`

```typescript
getOperatorId(): AccountId
```

### `getOperatorKey()`

```typescript
getOperatorKey(): PublicKey
```

### `setMaxTransactionFee()`

```typescript
setMaxTransactionFee(fee: Hbar): this
```

### `setMaxQueryPayment()`

```typescript
setMaxQueryPayment(payment: Hbar): this
```

### `close()`

```typescript
close()
```

### `close()`

```typescript
close(timeout: Timestamp)
```