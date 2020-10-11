# `ContractFunctionParameters`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`ADDRESS_LEN`](#address_len) | ✅ | ✅ | O
| [`ADDRESS_LEN_HEX`](#address_len_hex) | ✅ | ✅ | O
| [`SELECTOR_LEN`](#selector_len) | ✅ | ✅ | O
| [`SELECTOR_LEN_HEX`](#selector_len_hex) | ✅ | ✅ | O
| [`addString()`](#addstring) | ✅ | ✅ | O
| [`addStringArray()`](#addstringarray) | ✅ | ✅ | O
| [`addBytes()`](#addbytes) | ✅ | ✅ | O
| [`addBytesArray()`](#addbytesarray) | ✅ | ✅ | O
| [`addBytes32()`](#addbytes32) | ✅ | ✅ | O
| [`addBytes32Array()`](#addbytes32array) | ✅ | ✅ | O
| [`addBool()`](#addbool) | ✅ | ✅ | O
| [`addInt8()`](#addint8) | ✅ | ✅ | O
| [`addInt32()`](#addint32) | ✅ | ✅ | O
| [`addInt64()`](#addint64) | ✅ | ✅ | O
| [`addInt256()`](#addint256) | ✅ | ✅ | O
| [`addInt8Array()`](#addint8array) | ✅ | ✅ | O
| [`addInt32Array()`](#addint32array) | ✅ | ✅ | O
| [`addInt64Array()`](#addint64array) | ✅ | ✅ | O
| [`addInt256Array()`](#addint256array) | ✅ | ✅ | O
| [`addUint8()`](#adduint8) | ✅ | ✅ | O
| [`addUint32()`](#adduint32) | ✅ | ✅ | O
| [`addUint64()`](#adduint64) | ✅ | ✅ | O
| [`addUint256()`](#adduint256) | ✅ | ✅ | O
| [`addUint8Array()`](#adduint8array) | ✅ | ✅ | O
| [`addUint32Array()`](#adduint32array) | ✅ | ✅ | O
| [`addUint64Array()`](#adduint64array) | ✅ | ✅ | O
| [`addUint256Array()`](#adduint256array) | ✅ | ✅ | O
| [`addAddress()`](#addaddress) | ✅ | ✅ | O
| [`addAddressArray()`](#addaddressarray) | ✅ | ✅ | O
| [`addFunction()`](#addfunction) | ✅ | ✅ | O

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