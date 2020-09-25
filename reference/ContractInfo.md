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
| [`constructor()`](#constructor) | ✅ | ✅ | O
| [`toBytes()`](#tobytes) | ✅ | ✅ | O
| [`fromBytes`](#frombytes) | ✅ | ✅ | O

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

### `constructor()`

```typescript
constructor(
    contractId: ContractId,
    accountId: AccountId
    contractAccountId: String, 
    adminKey: Key,
    expirationTime: Timestamp,
    renewPeriod: Timestamp,
    storage: long,
    memo: string,
    balance: long)
```

### `fromBytes()`

```typescript
fromBytes(data: bytes): this
```

### `toBytes()`

```typescript
toBytes(): bytes
```

