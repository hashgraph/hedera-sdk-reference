# error `BadMnemonic`

## Fields

### `mnemonic: Mnemonic`

The mnemonic that failed validation.

### `reason: BadMnemonicReason`

The reason (out of [`BadMnemonicReason`](./BadMnemonicReason.md)) for which the mnemonic failed validation.

### `unknownWordIndicies: int[]`

The indices in the mnemonic that were not found in the BIP-39
standard English word list; if, the reason for validation failure was unknown words.

## Declaration

```typescript
class BadMnemonic extends Error {
    mnemonic: Mnemonic;

    reason: BadMnemonicReason;

    unknownWordIndicies: int[];
}
```

 * Each language have differing conventions for errors:
    * Java, Dart — `BadMnemonicException`
    * Rust, JavaScript, Python — `BadMnemonicError`
    * Go — `ErrBadMnemonic`
    * C — `HEDERA_BAD_MNEMONIC_UNKNOWN_WORDS`, etc.
