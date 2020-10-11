# `Mnemonic`

> class `Mnemonic`

<details>
<summary><b>Declaration</b></summary>

```typescript
class Mnemonic {
    static generate(): Mnemonic;

    static generateN(numWords: Uint): Mnemonic;

    static fromWords(words: string[]): Mnemonic;

    static fromString(text: string): Mnemonic;

    toPrivateKey(passphrase: string): PrivateKey;

    toString(): string;

    readonly words: string[];
}
```

</details>

Multi-word mnemonic phrases.

Compatible with (both original and current) Hedera mobile wallets
and MyHbarWallet.

### Static Methods

##### `generate` (): `Mnemonic`

Generate a new random 24-word mnemonic from the BIP-39 standard
English word list.

---

##### `generateN` ( `count`: `Uint` ): `Mnemonic`

Generate a new random `count`-word mnemonic from the BIP-39 standard
English word list.

---

##### `fromWords` ( `words`: `string[]` ): `Mnemonic`

Create a mnemonic from the given list of words.

###### Errors

 * [`BadMnemonic`](reference/error/BadMnemonic.md) — when the mnemonic contains words not found in the word list; there is a checksum mismatch; or, an unexpected number of words.

---

##### `fromString` ( `text`: `string` ): `Mnemonic`

###### Errors

 * [`BadMnemonic`](reference/error/BadMnemonic.md) — when the mnemonic contains words not found in the word list; there is a checksum mismatch; or, an unexpected number of words.

---

### Methods

##### `toPrivateKey` ( `passphrase`: `string` ): `PrivateKey`

---

##### `toString` (): `string`

---

## Fields

##### `words`: `string[]`

---
