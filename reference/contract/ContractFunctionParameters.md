# `ContractFunctionParameters`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`ADDRESS_LEN`](#address_len) | ✅ | ✅ | ✅
| [`ADDRESS_LEN_HEX`](#address_len_hex) | ✅ | ✅ | ✅
| [`SELECTOR_LEN`](#selector_len) | ✅ | ✅ | ✅
| [`SELECTOR_LEN_HEX`](#selector_len_hex) | ✅ | ✅ | ✅
| [`addString()`](#addstring) | ✅ | ✅ | ✅
| [`addStringArray()`](#addstringarray) | ✅ | ✅ | ✅
| [`addBytes()`](#addbytes) | ✅ | ✅ | ✅
| [`addBytesArray()`](#addbytesarray) | ✅ | ✅ | ✅
| [`addBytes32()`](#addbytes32) | ✅ | ✅ | ✅
| [`addBytes32Array()`](#addbytes32array) | ✅ | ✅ | ✅
| [`addBool()`](#addbool) | ✅ | ✅ | ✅
| [`addInt8()`](#addint8) | ✅ | ✅ | ✅
| [`addInt32()`](#addint32) | ✅ | ✅ | ✅
| [`addInt64()`](#addint64) | ✅ | ✅ | ✅
| [`addInt256()`](#addint256) | ✅ | ✅ | ✅
| [`addInt8Array()`](#addint8array) | ✅ | ✅ | ✅
| [`addInt32Array()`](#addint32array) | ✅ | ✅ | ✅
| [`addInt64Array()`](#addint64array) | ✅ | ✅ | ✅
| [`addInt256Array()`](#addint256array) | ✅ | ✅ | ✅
| [`addUint8()`](#adduint8) | ✅ | ✅ | ✅
| [`addUint32()`](#adduint32) | ✅ | ✅ | ✅
| [`addUint64()`](#adduint64) | ✅ | ✅ | ✅
| [`addUint256()`](#adduint256) | ✅ | ✅ | ✅
| [`addUint8Array()`](#adduint8array) | ✅ | ✅ | ✅
| [`addUint32Array()`](#adduint32array) | ✅ | ✅ | ✅
| [`addUint64Array()`](#adduint64array) | ✅ | ✅ | ✅
| [`addUint256Array()`](#adduint256array) | ✅ | ✅ | ✅
| [`addAddress()`](#addaddress) | ✅ | ✅ | ✅
| [`addAddressArray()`](#addaddressarray) | ✅ | ✅ | ✅
| [`addFunction()`](#addfunction) | ✅ | ✅ | ✅

## Constants

### `ADDRESS_LEN`

The length of a Solidity address in bytes.

```typescript
ADDRESS_LEN: int
```

### `ADDRESS_LEN_HEX`

The length of a hexadecimal-encoded Solidity address, in ASCII characters (bytes).

```typescript
ADDRESS_LEN_HEX: int
```

### `SELECTOR_LEN`

Function selector length in bytes.

```typescript
SELECTOR_LEN: int
```

### `SELECTOR_LEN_HEX`

Function selector length in hex characters.

```typescript
SELECTOR_LEN_HEX: int
```

## Methods

### `addString()`

```typescript
addString(param: string): this
```

### `addStringArray()`

```typescript
addStringArray(strings: string[]): this
```

### `addBytes()`

```typescript
addBytes(param: bytes): this
```

### `addBytesArray()`

```typescript
addBytesArray(param: byte[][]): this
```

### `addBytes32()`

```typescript
addBytes32(param: bytes): this
```

### `addBytes32Array()`

```typescript
addBytes32Array(param: byte[][]): this
```

### `addBool()`

```typescript
addBool(bool: boolean): this
```

### `addInt8()`

```typescript
addInt8(value: byte): this
```

### `addInt32()`

```typescript
addInt32(value: int): this
```

### `addInt64()`

```typescript
addInt64(value: long): this
```

### `addInt256()`

```typescript
addInt256(value: BigInteger): this
```

### `addInt8Array()`

```typescript
addInt8Array(intArray: bytes): this
```

### `addInt32Array()`

```typescript
addInt32Array(intArray: int[]): this
```

### `addInt64Array()`

```typescript
addInt64Array(intArray: long[]): this
```

### `addInt256Array()`

```typescript
addInt256Array(intArray: BigInteger): this
```

### `addUint8()`

```typescript
addUint8(value: byte): this
```

### `addUint32()`

```typescript
addUint32(value: int): this
```

### `addUint64()`

```typescript
addUint64(value: long): this
```

### `addUint256()`

```typescript
addUint256(value: BigInteger): this
```

### `addUint8Array()`

```typescript
addUint8Array(intArray: bytes): this
```

### `addUint32Array()`

```typescript
addUint32Array(intArray: int[]): this
```

### `addUint64Array()`

```typescript
addUint64Array(intArray: long[]): this
```

### `addUint256Array()`

```typescript
addUint256Array(intArray: BigInteger[]): this
```

### `addAddress()`

```typescript
addAddress(address: string): this
```

### `addAddressArray()`

```typescript
addAddressArray(addresses: string[]): this
```

### `addFunction()`

```typescript
addFunction(
    address: string, selector: bytes
    | address:string, selector: ContractFunctionSelector): this
```
