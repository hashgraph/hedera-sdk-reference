# `ContractCreateTransaction`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
[`constructor()`](#new) | ✅ | ✅ | ✅
[`setBytecodeFileId()`](#setBytecodeFileId) | ✅ | ✅ | ✅
[`setAdminKey()`](#setAdminKey) | ✅ | ✅ | ✅
[`setGas()`](#setGas) | ✅ | ✅ | ✅
[`setInitialBalance()`](#setInitialBalance) | ✅ | ✅ | ✅
[`setProxyAccountId()`](#setProxyAccountId) | ✅ | ✅ | ✅
[`setAutoRenewPeriod()`](#setAutoRenewPeriod) | ✅ | ✅ | ✅
[`setConstructorParams()`](#setConstructorParams) | ✅ | ✅ | ✅
[`setContractMemo()`](#setContractMemo) | ✅ | ✅ | ✅

## Methods

### `constructor()`

```typescript
constructor()
```

### `setBytecodeFileId()`

```typescript
setBytecodeFileId(id: FileId): this
```

### `setAdminKey()`

```typescript
setAdminKey(key: PublicKey): this
```

### `setGas()`

```typescript
setGas(gas: Uint64): this
```

### `setInitialBalance()`

```typescript
setInitialBalance(balance: Hbar): this
```

### `setProxyAccountId()`

```typescript
setProxyAccountId(id: AccountId): this
```

### `setAutoRenewPeriod()`

```typescript
setAutoRenewPeriod(period: Duration): this
```

### `setConstructorParams()`

```typescript
setConstructorParams(params: ContractFunctionParams): this
```

### `setContractMemo()`

```typescript
setContractMemo(memo: string): this
```
