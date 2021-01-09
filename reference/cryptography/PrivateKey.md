# `PrivateKey`

> class `PrivateKey` implements [`Key`](reference/cryptography/Key.md)

<details>
<summary><b>Declaration</b></summary>

```typescript
class PrivateKey implements Key {
    static generate(): PrivateKey;

    static fromBytes(data: bytes): PrivateKey;

    static fromString(text: string): PrivateKey;

    static fromMnemonic(mnemonic: string, passphrase: string): PrivateKey;

    static fromKeystore(data: bytes, passphrase: string): PrivateKey;

    static fromPem(text: string, passphrase: string): PrivateKey;

    isDerivable(): bool;

    derive(index: int): PrivateKey;

    getPublicKey(): PublicKey;

    sign(message: bytes): bytes;

    toBytes(): bytes;

    toString(): string;

    toKeystore(passphrase: string): bytes;
}
```

</details>

### Static Methods

##### `generate` (): `PrivateKey`

---

##### `fromBytes` ( `data`: `bytes` ): `PrivateKey`

Parses a private key from bytes.

---

##### `fromString` ( `text`: `string` ): `PrivateKey`

---

##### `readPem` ( `pem`: `Reader` ): `PrivateKey`

---

##### `fromPem` ( `pem`: `String` ): `PrivateKey`

---

##### `fromKeystore` ( `data`: `bytes`, `passphrase`: `string` ): `PrivateKey`

---

##### `fromLegacyMnemonic` ( `data`: `bytes`): `PrivateKey`

---

##### `fromMnemonic` ( `mnemonic`: `string`, `passphrase`: `string` ): `PrivateKey`

Recovers an ed25519 private key from a 24, 22, or 12 word mnemonic. 24 and
12 word mnemonics use a BIP-32 word list and SLIP-10 deriviation. 22 word
mnemonics use a legacy word list from the original Hedera mobile wallets.

###### Errors

- [`BadMnemonic`](reference/error/BadMnemonic.md) — when the mnemonic contains
  words not found in the word list; there is a checksum mismatch; or, an
  unexpected number of words.

###### Examples

<!-- tabs:start -->

###### ** Java **

```java
// use "" for an empty passphrase
var key = PrivateKey.generate();
var key = PrivateKey.fromBytes(bytes);
var key = PrivateKey.fromString("key");

var key = PrivateKey.fromMnemonic("word,word2,word3", "");
```

###### ** Go **

```go
// use "" for an empty passphrase
mnemonic, err := hedera.MnemonicFromString("word1,word2,word3");
if err != nil {
    println(err.Error())
}

key, err := mnemonicFromString.ToPrivateKey(passphrase)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Methods

##### `isDerivable` (): `boolean`

---

##### `derive` ( `index`: `Uint` ): `PrivateKey`

---

##### `sign` ( `message`: `bytes` ): `bytes`

---

##### `signTransaction` ( `transaction`: `Transaction<?>` ): `bytes`

---

##### `toBytes` (): `bytes`

Converts this key into bytes.

---

##### `toString` (): `string`

---

##### `toKeystore` ( `passphrase`: `string` ): `bytes`

---

### Properties

##### `publicKey`: `PublicKey`

---
