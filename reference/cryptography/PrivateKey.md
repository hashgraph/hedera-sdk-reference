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

Parses a private key from bytes.

---

##### `fromBytesDer` ( `data`: `bytes` ): `PrivateKey`

Parses a private key from a DER endcoded private key.

---

##### `fromBytesEcdsa` ( `data`: `bytes` ): `PrivateKey`

Parses a private key from raw bytes for ECDSA.

---

##### `fromBytesEd25519` ( `data`: `bytes` ): `PrivateKey`

Parses a private key from raw bytes for Ed25519.

---

##### `fromString` ( `text`: `String` ): `PrivateKey`

Recovers a PrivateKey from its DER encoded representation.

Use `fromStringEcdsa()` or `fromStringEd25519()` to create a `PrivateKey` from bytes without a DER prefix

---

##### `fromStringEcdsa` ( `text`: `String` ): `PrivateKey`

Recovers a ECDSA PrivateKey from its text-encoded representation.

---

##### `fromStringEd25519` ( `text`: `String` ): `PrivateKey`

Recovers a Ed25519 PrivateKey from its text-encoded representation.

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

Outputs the private key with a DER header 

---

##### `toBytesDer` ( ): `bytes`

Outputs the private key with a DER header 

---

##### `toBytesRaw` ( ): `bytes`

Outputs just the private key bytes without the DER header

---

##### `toString` ( ): `String`

Serialiazes the private key with a DER header into string representation

---

##### `toStringDer` ( ): `String`

Serializes just the private key bytes without the DER header

---

##### `toStringRaw` ( ): `String`

Serialiazes the private key without a DER header into string representation

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
