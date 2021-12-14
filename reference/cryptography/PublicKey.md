> class `PublicKey` implements [`Key`](reference/cryptography/Key.md)

A public key on the Hedera™ network.

<!-- tabs:start -->

###### ** Java **

```java
var publicKey = PublicKey.fromString("...");
```

### ** JavaScript **

```javascript
const publicKey = PublicKey.fromString("...");
```

###### ** Go **

```go
publicKey, err := hedera.PublicKeyFromString("...")
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Static Methods

##### `fromString` ( `text`: `String` ): `PublicKey`

Parse a public key from a hex encoded public key with a DER header.

---

##### `fromStringEcdsa` ( `text`: `String` ): `PublicKey`

Parse a ECDSA public key from a string of hexadecimal digits.

---

##### `fromStringEd25519` ( `text`: `String` ): `PublicKey`

Parse a Ed25519 public key from a string of hexadecimal digits.

---

##### `fromBytes` ( `data`: `bytes` ): `PublicKey`

Parses a public key from bytes with a DER header.

---

##### `fromBytesEcdsa` ( `data`: `bytes` ): `PublicKey`

Parses a ECDSA public key from bytes.

---

##### `fromBytesEd25519` ( `data`: `bytes` ): `PublicKey`

Parses a Ed25519 public key from bytes.

---

### Methods

##### `verify` ( `message`: `bytes`, `signature`: `bytes` ): `bool`

Verify the signature on the message with this public key.

---

##### `verifyTransaction` ( `transaction`: [`Transaction`](reference/core/Transaction.md) ): `bool`

Verify the signatures on all the messages in the Transaction.

---

##### `toBytes` (): `bytes`

Outputs the public key with a DER header 

---

##### `toBytesDer` ( ): `bytes`

Outputs the public key with a DER header 

---

##### `toBytesRaw` ( ): `bytes`

Outputs just the public key bytes without the DER header

---

##### `toString` ( ): `String`

See: [`toStringDer()`](#tostringder-string)

---

##### `toStringDer` ( ): `String`

Encodes the public key using SPKI, DER, and HEX. This results in
a string which has the key data of the public key prefixed with
a header.


The header for Ed25519 is: "302a300506032b6570032100"
The header for ECDSA is: "302f300706052b8104000a0324000421"

---

##### `toStringRaw` ( ): `String`

Encodes the private key data into HEX with no header.

---


##### `toAccountId` ( `shard`: `Uint64`, `realm`: `Uint64` ): `AccountId`

Convert this public key into an account ID with a given shard and realm.

---
