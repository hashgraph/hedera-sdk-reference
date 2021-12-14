> class `PrivateKey` implements [`Key`](reference/cryptography/Key.md)

A private key on the Hedera™ network.

> [!TIP]
>  Use "" for an empty passphrase

<!-- tabs:start -->

#### ** Java **

```java
var key = PrivateKey.generate();
var key = PrivateKey.fromBytes(bytes);
var key = PrivateKey.fromString("key");
var key = PrivateKey.fromPem(pemString, passphrase);

var key = PrivateKey.fromMnemonic("word word2 word3", passphrase);
```

#### ** JavaScript **

```javascript
const key = PrivateKey.generate()
const key = PrivateKey.fromBytes(bytes);
const key = PrivateKey.fromString("key")
const key = await PrivateKey.fromPem(pemString, passphrase)
const key = await PrivateKey.fromKeystore(keystoreBytes, passphrase)

const mnemonic = await Mnemonic.fromString("word1 word2 word3...");
const key = PrivateKey.fromMnemonic(mnemonic, passphrase)
```

#### ** Go **

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

##### `generate` ( ): `PrivateKey`

Generates a new Ed25519 private key.

Deprecated: Use `generateEd5519()` or `generateEcdsa()` instead.

---

##### `generateEcdsa` ( ): `PrivateKey`

Generates a new ECDSA private key.

---

##### `generateEd25519` ( ): `PrivateKey`

Generates a new Ed25519 private key.

---

##### `fromBytes` ( `data`: `bytes` ): `PrivateKey`

Parses a DER encoded Ed25519 or ECDSA private key

**Note**: The use of raw bytes for a Ed25519 private key is deprecated; use `fromBytesEd25519()` instead.

---

##### `fromBytesDer` ( `data`: `bytes` ): `PrivateKey`

Parses a DER encoded Ed25519 or ECDSA private key

**Note**: Does **not** support raw bytes; the data provided must be DER encoded.

---

##### `fromBytesEcdsa` ( `data`: `bytes` ): `PrivateKey`

Parses an ECDSA private key from either DER encoded or raw bytes.

---

##### `fromBytesEd25519` ( `data`: `bytes` ): `PrivateKey`

Parses an Ed25519 private key from either DER encoded or raw bytes.

---

##### `fromString` ( `text`: `String` ): `PrivateKey`

Parses a HEX and DER encoded Ed25519 or ECDSA private key

**Note**: The use of raw bytes for a Ed25519 private key is deprecated; use `fromStringEd25519()` instead.

---

##### `fromStringDer` ( `text`: `String` ): `PrivateKey`

Parses a HEX and DER encoded Ed25519 or ECDSA private key

**Note**: Does **not** support raw bytes; the data provided must be DER encoded.

---

##### `fromStringEcdsa` ( `text`: `String` ): `PrivateKey`

Parses an ECDSA private key from either HEX and DER encoded bytes or just HEX encoded raw bytes.

---

##### `fromStringEd25519` ( `text`: `String` ): `PrivateKey`

Parses an Ed25519 private key from either HEX and DER encoded bytes or just HEX encoded raw bytes.

---

##### `fromPem` ( `pem`: `String` ): `PrivateKey`

Parse a private key from a PEM encoded string.

---

##### `fromKeystore` ( `data`: `bytes`, `passphrase`: `String` ): `PrivateKey`

Recovers an PrivateKey from an encrypted keystore encoded as a byte slice.

---

##### `fromMnemonic` ( `mnemonic`: `String`, `passphrase`: `String` ): `PrivateKey`

Recovers an ed25519 private key from a 24, 22, or 12 word mnemonic. 24 and
12 word mnemonics use a BIP-32 word list and SLIP-10 deriviation. 22 word
mnemonics use a legacy word list from the original Hedera mobile wallets.

###### Errors

- [`BadMnemonic`](reference/error/BadMnemonic.md) — when the mnemonic contains
  words not found in the word list; there is a checksum mismatch; or, an
  unexpected number of words.

### Methods

##### `isDerivable` ( ): `boolean`

Check if this private key supports derivation.

---

##### `derive` ( `index`: `Uint` ): `PrivateKey`

Given a wallet/account index, derive a child key compatible with the iOS and Android wallets.

---

##### `sign` ( `message`: `bytes` ): `bytes`

Sign a message with this private key.

---

##### `signTransaction` ( `transaction`: [`Transaction`](reference/core/Transaction.md) ): `bytes`

Sign a transaction with this private key.

---

##### `toBytes` ( ): `bytes`

Serialize the private key into bytes.

**Note**: For `Ed25519` the result of this method call is identical to `toBytesRaw()` while for `ECDSA`
this method is identical to `toBytesDer()`.

We strongly recommend using `toBytesRaw()` or `toBytesDer()` instead.

---

##### `toBytesDer` ( ): `bytes`

Serialize the private key into bytes using PKCS and DER encoding.

---

##### `toBytesRaw` ( ): `bytes`

Return just the raw bytes for the given key.

---

##### `toString` ( ): `String`

See: [`toStringDer()`](#tostringder-string)

---

##### `toStringDer` ( ): `String`

Encodes [`toBytesDer()`](#tostringder-string) into HEX.

**Note**: This results in a string which has the key data of the private key prefixed with a header.

The header for Ed25519 is: "302e020100300506032b657004220420"

The header for ECDSA is: "3030020100300706052b8104000a04220420"

---

##### `toStringRaw` ( ): `String`

Encodes [`toBytesRaw()`](#tostringder-string) into HEX.

---

##### `toKeystore` ( `passphrase`: `String` ): `bytes`

Converts the private key into a keystore which can be saved on disk

---

##### `toAccountId` ( `shard`: `Uint64`, `realm`: `Uint64` ): `AccountId`

Convert this private key into an account ID with a given shard and realm.

Note: The account ID created will use the `publicKey` property of this `PrivateKey`,
not the `PrivateKey` bytes.

---

### Properties

##### `publicKey`: [`PublicKey`](reference/cryptography/PublicKey.md)

Derive a public key from this private key.

---
