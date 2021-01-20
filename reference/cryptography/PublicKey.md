# `PublicKey`

> class `PublicKey` implements [`Key`](reference/cryptography/Key.md)

<details>
<summary><b>Declaration</b></summary>

```typescript
class PublicKey implements Key, Eq<PublicKey> {
    static fromBytes(data: bytes): PublicKey;

    static fromString(text: string): PublicKey;

    verify(message: bytes, signature: bytes): bool;

    verifyTransaction(transaction: Transaction<?>): bool;

    equals(other: PublicKey): bool;

    toBytes(): bytes;

    toString(): string;
}
```

</details>

A public key on the Hedera™ network.

### Static Methods

##### `fromString` ( `text`: `String` ): `PublicKey`

Parse a public key from a string of hexadecimal digits.

The public key may optionally be prefixed with the DER header.

##### `fromBytes` ( `data`: `bytes` ): `PublicKey`

Parses a public key from bytes.

### Methods

##### `verify` ( `message`: `bytes`, `signature`: `bytes` ): `bool`

Verify the signature on the message with this public key.

##### `verifyTransaction` ( `transaction`: `Transaction<?>`): `bool`

Verify the signatures on all the messages in the Transaction.

##### `equals` ( `other`: `PublicKey` ): `bool`

Returns `true` if this public key is the same as the
public key at `other`.

Note that this method may be different across different SDKs to conform
to the equality interface or protocol.

##### `toBytes` (): `bytes`

Converts this key into bytes.

##### `toString` (): `String`

Returns the public key as a string with the DER prefix
that identifies the algorithim.

##### `hashCode` (): `int`

---

```js
publicKey.toString();
// 302a300506032b6570032100a1e0fa8780be3ef75f348cc280be11e5d2f19b72ef41ffdb745cd50d5eea9a99
// 302a300506032b6570032100 is the DER prefix identifying this key as ED25519
```
