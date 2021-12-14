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

##### `toString` (): `String`

Returns the public key as a string with the DER prefix that identifies the algorithim.

---

##### `toStringDer` ( ): `String`

Serializes just the public key bytes without the DER header

---

##### `toStringRaw` ( ): `String`

Serialiazes the public key without a DER header into string representation

---

##### `toAccountId` ( `shard`: `Uint64`, `realm`: `Uint64` ): `AccountId`

Convert this public key into an account ID with a given shard and realm.

---
