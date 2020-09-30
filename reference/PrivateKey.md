# `PrivateKey`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`generate()`](#generate) | ✅ | ✅ | O
| [`fromBytes()`](#frombytes) | ✅ | ✅ | O
| [`toBytes()`](#tobytes) | ✅ | ✅ | O
| [`fromString()`](#fromstring) | ✅ | ✅ | O
| [`fromMnemonic()`](#frommnemonic) | ✅ | ✅ | O
| [`readPem()`](#readpem) | ✅ | ✅ | O
| [`fromPem()`](#frompem) | ✅ | ✅ | O
| [`isDerivable()`](#isderivable) | ✅ | ✅ | O
| [`derive()`](#derive) | ✅ | ✅ | O
| [`getPublicKey()`](#getpublickey) | ✅ | ✅ | O
| [`sign()`](#sign) | ✅ | ✅ | O
| [`toDER()`](#toder) | ✅ | ✅ | O

## Methods

### `generate()`

```typescript
generate(): this
```

### `toBytes()`

```typescript
toBytes(): bytes
```

### `fromString()`

```typescript
fromString(key: string): this
```

### `fromString()`

```typescript
fromString(key: string): this
```

### `fromMnemonic()`

```typescript
fromMnemonic(
    mnemonic: Mnemonic,
    passphrase: string 
    | mnemonic: Mnemonic ): this
```

### `readPem()`

```typescript
readPem(
    pemFile: Reader 
    | pemFile: Reader, password: string): this
```

### `fromPem()`

```typescript
fromPem(
    pemEncoded: string
    | pemEncoded: string, password: string): this
```

### `isDerivable()`

```typescript
isDerivable(): boolean
```

### `derive()`

```typescript
derive(index: int): this
```

### `getPublicKey()`

```typescript
getPublicKey(): PublicKey
```

### `sign()`

```typescript
sign(message: bytes): bytes
```

### `toDER()`

```typescript
toDER(): bytes
```