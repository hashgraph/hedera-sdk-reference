> class `PublicKey` implements [`Key`](reference/cryptography/Key.md)

A public key on the Hedera™ network.

<!-- tabs:start -->

### ** Java **

```java
var publicKey = PublicKey.fromString("...");
```

### ** JavaScript **

```javascript
const publicKey = PublicKey.fromString("...");
```

### ** Go **

```go
publicKey, err := hedera.PublicKeyFromString("...")
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Static Methods

##### `fromString` ( `text`: `String` ): `PublicKey`

Parses a HEX and DER encoded Ed25519 or ECDSA public key

**Note**: The use of raw bytes for a Ed25519 public key is deprecated; use `fromStringEd25519()` instead.

---

##### `fromStringDer` ( `text`: `String` ): `PublicKey`

Parses a HEX and DER encoded Ed25519 or ECDSA public key

**Note**: Does **not** support raw bytes; the data provided must be DER encoded.

---

##### `fromStringEcdsa` ( `text`: `String` ): `PublicKey`

Parses an ECDSA public key from either HEX and DER encoded bytes or just HEX encoded raw bytes.

---

##### `fromStringEd25519` ( `text`: `String` ): `PublicKey`

Parses an Ed25519 public key from either HEX and DER encoded bytes or just HEX encoded raw bytes.

---

##### `fromBytes` ( `data`: `bytes` ): `PublicKey`

Parses a DER encoded Ed25519 or ECDSA public key

**Note**: The use of raw bytes for a Ed25519 public key is deprecated; use `fromBytesEd25519()` instead.

---

##### `fromBytesDer` ( `data`: `bytes` ): `PublicKey`

Parses a DER encoded Ed25519 or ECDSA public key

**Note**: Does **not** support raw bytes; the data provided must be DER encoded.

---

##### `fromBytesEcdsa` ( `data`: `bytes` ): `PublicKey`

Parses an ECDSA public key from either DER encoded or raw bytes.

---

##### `fromBytesEd25519` ( `data`: `bytes` ): `PublicKey`

Parses an Ed25519 public key from either DER encoded or raw bytes.

---

### Methods

##### `verify` ( `message`: `bytes`, `signature`: `bytes` ): `bool`

Verify the signature on the message with this public key.

---

##### `verifyTransaction` ( `transaction`: [`Transaction`](reference/core/Transaction.md) ): `bool`

Verify the signatures on all the messages in the Transaction.

---

##### `toBytes` ( ): `bytes`

Serialize the private key into bytes.

**Note**: For `Ed25519` the result of this method call is identical to `toBytesRaw()` while for `ECDSA`
this method is identical to `toBytesDer()`.

We strongly recommend using `toBytesRaw()` or `toBytesDer()` instead.

---

##### `toBytesDer` ( ): `bytes`

Serialize the private key into bytes using SPKI and DER encoding.

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

The header for Ed25519 is: "302a300506032b6570032100"

The header for ECDSA is: "302f300706052b8104000a0324000421"

---

##### `toStringRaw` ( ): `String`

Encodes [`toBytesRaw()`](#tostringder-string) into HEX.

---

##### `toAccountId` ( `shard`: `Uint64`, `realm`: `Uint64` ): `AccountId`

Convert this public key into an account ID with a given shard and realm.

---

##### `toEvmAddress` (): `string`

Convert this public key into an evm address. The EVM address is This is the rightmost 20 bytes of the 32 byte Keccak-256 hash of the ECDSA public key. 

---
