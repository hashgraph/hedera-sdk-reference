# `BadMnemonic`

> error `BadKey`

<details>
<summary><b>Declaration</b></summary>

```typescript
class BadMnemonicError extends Error {
    readonly mnemonic: Mnemonic;

    readonly reason: BadMnemonicReason;

    readonly unknownWordIndicies: int[];
}
```

</details>

-   Each language has differing conventions for errors:
    -   Java, Dart — `BadMnemonicException`
    -   Rust, JavaScript, Python — `BadMnemonicError`
    -   Go — `ErrBadMnemonic`
    -   C — `HEDERA_BAD_MNEMONIC_UNKNOWN_WORDS`, etc.

### Fields

##### `mnemonic`: `Mnemonic`

The mnemonic that failed validation.

---

##### `reason`: [`BadMnemonicReason`](reference/error/BadMnemonicReason.md)

The reason for which the mnemonic failed validation.

---

##### `unknownWordIndicies`: `Uint[]`

The indices in the mnemonic that were not found in the BIP-39
standard English word list; if, the reason for validation failure was unknown words.

---
