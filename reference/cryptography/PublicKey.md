> class `PublicKey` implements [`Key`](reference/cryptography/Key.md)

A public key on the Hedera™ network.

<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`fromString()`](#fromstring-text-string-public-key) | ✅ | ✅ | ✅
| [`fromBytes()`](#from-bytes-data-bytes-publickey) | ✅ | ✅ | ✅
| [`verify()`](#verify-message-bytes-signature-bytes-bool) | ✅ | ✅ | ✅
| [`verifyTransaction()`](#verifytransaction-transaction-transaction-bool) | ✅ | ✅ | ✅
| [`equals()`](#equals-other-publickey-bool) | ✅ | ✅ | ✅
| [`toBytes()`](#tobytes-bytes) | ✅ | ✅ | ✅
| [`toString()`](#tostring-string) | ✅ | ✅ | ✅
| [`hasCode()`](#hascode-int64) | ✅ | ✅ | ✅
</details>

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

##### `fromString` ( `text`: `String` ): [`PublicKey`](#)

Parse a public key from a string of hexadecimal digits.

The public key may optionally be prefixed with the DER header.

##### `fromBytes` ( `data`: `bytes` ): [`PublicKey`](#)

Parses a public key from bytes.

### Methods

##### `verify` ( `message`: `bytes`, `signature`: `bytes` ): `bool`

Verify the signature on the message with this public key.

##### `verifyTransaction` ( `transaction`: [`Transaction`](reference/core/Transaction.md) ): `bool`

Verify the signatures on all the messages in the Transaction.

##### `equals` ( `other`: [`PublicKey`](#) ): `bool`

Returns `true` if this public key is the same as the
public key at `other`.

Note that this method may be different across different SDKs to conform
to the equality interface or protocol.

##### `toBytes` (): `bytes`

Converts this key into bytes.

##### `toString` (): `String`

Returns the public key as a string with the DER prefix
that identifies the algorithim.

##### `hashCode` (): `Uint64`

---
