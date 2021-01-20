> class `PrivateKey` implements [`Key`](reference/cryptography/Key.md)

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`generate()`](#generate-privatekey) | ✅ | ✅ | ✅
| [`fromMnemonic()`](#frommnemonic-mnemonic-string-passphrase-string-privatekey) | ✅ | ✅ | ✅
| [`fromString()`](#fromstring-text-string-privatekey) | ✅ | ✅ | ✅
| [`fromBytes()`](#frombytes-data-bytes-privatekey) | ✅ | ✅ | ✅
| [`readPem()`](#readpem-pem-reader-privatekey) | ✅ | ✅ | ✅
| [`fromPem()`](#frompem-pem-string-privatekey) | ✅ | ✅ | ✅
| [`isDerivable()`](#isderivable-boolean) | ✅ | ✅ | ✅
| [`derive()`](#derive-index-uint-privatekey) | ✅ | ✅ | ✅
| [`publicKey`](#publickey-publickey) | ✅ | ✅ | ✅
| [`sign()`](#sign-message-bytes-bytes) | ✅ | ✅ | ✅
| [`signTransaction()`](#signtransaction-transaction-transaction-bytes) | ✅ | ✅ | ✅
| [`toBytes()`](#tobytes-bytes) | ✅ | ✅ | ✅
| [`toString()`](#tostring-string) | ✅ | ✅ | ✅
| [`fromLegacyMnemonic()`](#fromlegacymnemonic-data-bytes-privatekey) | ✅ | ✅ | ✅
</details>

> [!TIP]
>  Use "" for an empty passphrase

<!-- tabs:start -->

###### ** Java **

```java
var key = PrivateKey.generate();
var key = PrivateKey.fromBytes(bytes);
var key = PrivateKey.fromString("key");
var key = PrivateKey.fromPem(pemString, passphrase);

var key = PrivateKey.fromMnemonic("word word2 word3", passphrase);
```

### ** JavaScript **

```javascript
const key = PrivateKey.generate()
const key = PrivateKey.fromBytes(bytes);
const key = PrivateKey.fromString("key")
const key = await PrivateKey.fromPem(pemString, passphrase)
const key = await PrivateKey.fromKeystore(keystoreBytes, passphrase)

const mnemonic = await Mnemonic.fromString("word1 word2 word3...");
const key = PrivateKey.fromMnemonic(mnemonic, passphrase)
```

###### ** Go **

```go
newKey, err := GeneratePrivateKey()
newKey, err := PrivateKeyFromBytes(bytes)
newKey, err := PrivateKeyFromString("key")
newKey, err := PrivateKeyFromKeystore(bytes, passphrase)
newKey, err := PrivateKeyFromPem(bytes, passphrase)
if err != nil {
    println(err.Error())
}

// use "" for an empty passphrase
mnemonic, err := hedera.MnemonicFromString("word1 word2 word3...");
if err != nil {
    println(err.Error())
}

key, err := mnemonic.ToPrivateKey(passphrase)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Static Methods

##### `generate` (): [`PrivateKey`](#)

Generates a new Ed25519 private key.

---

##### `fromBytes` ( `data`: `bytes` ): [`PrivateKey`](#)

Parses a private key from bytes.

---

##### `fromString` ( `text`: `String` ): [`PrivateKey`](#)

Recovers an PrivateKey from its text-encoded representation.

---

##### `readPem` ( `pem`: `Reader` ): [`PrivateKey`](#)

Parse a private key from a PEM encoded reader.
This will read the first "PRIVATE KEY" section in the stream as an Ed25519 private key.

---

##### `fromPem` ( `pem`: `String` ): [`PrivateKey`](#)

Parse a private key from a PEM encoded string.

---

##### `fromKeystore` ( `data`: `bytes`, `passphrase`: `String` ): [`PrivateKey`](#)

Recovers an PrivateKey from an encrypted keystore encoded as a byte slice.

---

##### `fromLegacyMnemonic` ( `data`: `bytes`): [`PrivateKey`](#)

Recovers an ed25519 private key from a  22 word mnemonic, using legacy word list.

---

##### `fromMnemonic` ( `mnemonic`: `String`, `passphrase`: `String` ): [`PrivateKey`](#)

Recovers an ed25519 private key from a 24, 22, or 12 word mnemonic. 24 and
12 word mnemonics use a BIP-32 word list and SLIP-10 deriviation. 22 word
mnemonics use a legacy word list from the original Hedera mobile wallets.

###### Errors

- [`BadMnemonic`](reference/error/BadMnemonic.md) — when the mnemonic contains
  words not found in the word list; there is a checksum mismatch; or, an
  unexpected number of words.

### Methods

##### `isDerivable` (): `boolean`

Check if this private key supports derivation.

---

##### `derive` ( `index`: `Uint` ): [`PrivateKey`](#)

Given a wallet/account index, derive a child key compatible with the iOS and Android wallets.

---

##### `sign` ( `message`: `bytes` ): `bytes`

Sign a message with this private key.

---

##### `signTransaction` ( `transaction`: [`Transaction`](reference/core/Transaction.md) ): `bytes`

Sign a transaction with this private key.

---

##### `toBytes` (): `bytes`

Converts this key into bytes.

---

##### `toString` (): `String`

---

##### `toKeystore` ( `passphrase`: `String` ): `bytes`

---

### Properties

##### `publicKey`: [`PublicKey`](reference/cryptography/PublicKey.md)

Derive a public key from this private key.

---
