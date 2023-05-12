> class `Mnemonic`

Multi-word mnemonic phrases.

Compatible with (both original and current) Hedera mobile wallets
and MyHbarWallet.

<!-- tabs:start -->

### ** Java **

```java
var mnemonic = Mnemonic.fromString(words);

var privateKey = mnemonic.toStandardEd25519PrivateKey("", 0);
var privateKey = mnemonic.toStandardECDSAsecp256k1PrivateKey("", 0);
var legacyPrivateKey = mnemonic.toLegacyPrivateKey();
```

### ** JavaScript **

```javascript
const mnemonic = Mnemonic.fromString(words);

const privateKey = await mnemonic.toPrivateKey();
const legacyPrivateKey = await mnemonic.toLegacyPrivateKey();
```

### ** Go **

```go
mnemonic := MnemonicFromString(words);

privateKey := mnemonic.ToPrivateKey();
legacyPrivateKey := mnemonic.ToLegacyPrivateKey();
```

<!-- tabs:end -->
### Static Methods

##### `fromString` ( `text`: `String` ): `Mnemonic`

Deserialize a mnemonic from a string containing a list of words separated by spaces

###### Errors

- [`BadMnemonic`](../error/BadMnemonic.md) — when the mnemonic contains
  words not found in the word list; there is a checksum mismatch; or, an
  unexpected number of words.

---

##### `fromWords` ( `words`: `String[]` ): `Mnemonic`

Create a mnemonic from the given list of words.

###### Errors

- [`BadMnemonic`](../error/BadMnemonic.md) — when the mnemonic contains
  words not found in the word list; there is a checksum mismatch; or, an
  unexpected number of words.

---

##### `generate12` ( ): `Mnemonic`

Returns a new random 12-word mnemonic from the BIP-39 standard English word list.

---

##### `generate24` ( ): `Mnemonic`

Returns a new random 24-word mnemonic from the BIP-39 standard English word list.

### Methods

##### `toPrivateKey` ( `passphrase`: `String` ): [`PrivateKey`](PrivateKey.md)

Derive a private key from the current mnemonic

---

##### `toStandardECDSAsecp256k1PrivateKey` ( `passphrase`: `String`, `index`: `Uint32` ): [`PrivateKey`](PrivateKey.md)

Recover an ECDSAsecp256k1 private key from the mnemonic phrase, with an optional passphrase.

---

##### `toStandardEd25519PrivateKey` ( `passphrase`: `String`, `index`: `Uint32` ): [`PrivateKey`](PrivateKey.md)

Recover an Ed25519 private key from the mnemonic phrase, with an optional passphrase.

---

##### `toString` ( ): `String`

Serializes mnemonic into string where the words are separated by spaces

---

### Properties

##### `words`: `String[]`

The list of words that define this mnemonic
