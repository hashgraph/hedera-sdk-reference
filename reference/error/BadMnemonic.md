# error `BadMnemonic`

<details>
<summary>Declaration</summary>

```typescript
class BadMnemonicError extends Error {
    mnemonic: Mnemonic;

    reason: BadMnemonicReason;

    unknownWordIndicies: int[];
}
```

</details>

-   Each language has differing conventions for errors:
    -   Java, Dart — `BadMnemonicException`
    -   Rust, JavaScript, Python — `BadMnemonicError`
    -   Go — `ErrBadMnemonic`
    -   C — `HEDERA_BAD_MNEMONIC_UNKNOWN_WORDS`, etc.

## Fields

### `mnemonic`

```typescript
mnemonic: Mnemonic;
```

The mnemonic that failed validation.

### `reason`

```typescript
reason: BadMnemonicReason;
```

The reason (out of [`BadMnemonicReason`](./BadMnemonicReason.md)) for which the mnemonic failed validation.

### `unknownWordIndicies`

```typescript
unknownWordIndicies: int[];
```

The indices in the mnemonic that were not found in the BIP-39
standard English word list; if, the reason for validation failure was unknown words.
