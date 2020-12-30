# `ContractInfo`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`contractId`](#contractid) | ✅ | ✅ | ✅
| [`accountId`](#accountid) | ✅ | ✅ | ✅
| [`contractAccountId`](#contractaccountid) | ✅ | ✅ | ✅
| [`adminKey`](#adminkey) | ✅ | ✅ | ✅
| [`expirationTime`](#expirationtime) | ✅ | ✅ | ✅
| [`autoRenewPeriod`](#autorenewperiod) | ✅ | ✅ | ✅
| [`storage`](#storage) | ✅ | ✅ | ✅
| [`contractMemo`](#contractmemo) | ✅ | ✅ | ✅
| [`balance`](#balance) | ✅ | ✅ | ✅
| [`toBytes()`](#tobytes) | ✅ | ✅ | ✅
| [`fromBytes`](#frombytes) | ✅ | ✅ | ✅

## Fields

### `contractId`

```typescript
contractId: ContractId
```

### `accountId`

```typescript
accountId: AccountId
```

### `contractAccountId`

```typescript
contractAccountId: string
```

### `adminKey`

```typescript
adminKey: Key
```

### `expirationTime`

```typescript
expirationTime: Timestamp
```

### `autoRenewPeriod`

```typescript
autoRenewPeriod: Timestamp
```

### `storage`

```typescript
storage: long
```

### `contractMemo`

```typescript
contractMemo: string
```

### `balance`

```typescript
balance: Hbar
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

