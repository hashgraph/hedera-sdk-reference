# class `Mnemonic`

Multi-word mnemonic phrases.

Compatible with (both original and current) Hedera mobile wallets
and MyHbarWallet.

## Static Methods

### `generate(): Mnemonic`

Generate a new random 24-word mnemonic from the BIP-39 standard
English word list.

#### Examples

###### Python

```python
mnemonic = Mnemonic.generate()
# admit forum pond diet risk true cat retreat skull typical coffee special divert measure canyon valley disorder exist column grain switch drink real employ
```

### `generate12(): Mnemonic`

Generate a new random 12-word mnemonic from the BIP-39 standard
English word list.

### `fromWords(words: string[]): Mnemonic`

#### Errors

 * [`BadMnemonic`](./BadMnemonic.md) — when the mnemonic contains words not found in the word list; there is a checksum mismatch; or, an unexpected number of words.

### `fromString(text: string): Mnemonic`

#### Errors

 * [`BadMnemonic`](./BadMnemonic.md) — when the mnemonic contains words not found in the word list; there is a checksum mismatch; or, an unexpected number of words.

## Methods

### `toPrivateKey(passphrase: string): PrivateKey`

### `toString(): string`

## Fields

### `words: string[]`

## Declaration

```typescript
class Mnemonic {
    static generate(): Mnemonic;

    static generate12(): Mnemonic;

    static fromWords(words: string[]): Mnemonic;

    static fromString(text: string): Mnemonic;

    toPrivateKey(passphrase: string): PrivateKey;

    toString(): string;

    words: string[];
}
```
