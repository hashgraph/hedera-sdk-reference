> class `Mnemonic`

Multi-word mnemonic phrases.

Compatible with (both original and current) Hedera mobile wallets
and MyHbarWallet.

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`generate()`](#generate-mnemonic) | ✅ | ✅ | ✅
| [`generateN()`](#generaten-count-uint-mnemonic) | ✅ | ✅ | ✅
| [`fromWords()`](#fromwrods-words-string-mnemonic) | ✅ | ✅ | ✅
| [`fromString()`](#fromstring-text-string-mnemonic) | ✅ | ✅ | ✅
| [`toPrivateKey()`](#toprivatekey-passphrase-string-privatekey) | ✅ | ✅ | ✅
| [`toString()`](#tostring-string) | ✅ | ✅ | ✅
| [`words`](#words-string) | ✅ | ✅ | ✅
</details>

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

- [`BadMnemonic`](reference/error/BadMnemonic.md) — when the mnemonic contains
  words not found in the word list; there is a checksum mismatch; or, an
  unexpected number of words.

---

##### `fromString` ( `text`: `String` ): `Mnemonic`

###### Errors

- [`BadMnemonic`](reference/error/BadMnemonic.md) — when the mnemonic contains
  words not found in the word list; there is a checksum mismatch; or, an
  unexpected number of words.

---

### Methods

##### `toPrivateKey` ( `passphrase`: `String` ): [`PrivateKey`](reference/cryptography/PrivateKey.md)

---

##### `toString` (): `String`

---

### Properites

##### `words`: `string[]`

---
