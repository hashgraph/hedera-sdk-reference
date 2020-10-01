# `enum BadMnemonicReason`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#constructor) | ✅ | ✅ | ✅

## Variants

### `BadLength`

The mnemonic did not contain exactly 24 words.

```typescript
BadLength
```

### `UnknownWords`

The mnemonic contained words which were not found in the BIP-39 standard English word list.

```typescript
UnknownWords
```

### `ChecksumMismatch`

The checksum encoded in the mnemonic did not match the checksum we just calculated for that mnemonic.
```typescript
ChecksumMismatch
```