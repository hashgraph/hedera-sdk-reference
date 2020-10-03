# class `PublicKey`

A public key on the Hedera™ network.

## Static Methods

### `fromString(text: string): PublicKey`

Parse a public key from a string of hexadecimal digits.

The public key may optionally be prefixed with the DER header.

## Methods

### `verify(message: bytes, signature: bytes): bool`

Verify the signature on the message with this public key.

### `equals(other: PublicKey): bool`

Returns `true` if this public key is the same as the
public key at `other`.

### `toString(): string`

Returns the public key as a string with the DER prefix
that identifies the algorithim.

```js
publicKey.toString();
// 302a300506032b6570032100a1e0fa8780be3ef75f348cc280be11e5d2f19b72ef41ffdb745cd50d5eea9a99
// 302a300506032b6570032100 is the DER prefix identifying this key as ED25519
```

## Declaration

```typescript
class PublicKey implements Key {
    static fromString(text: string): PublicKey;

    verify(message: bytes, signature: bytes): bool;

    equals(other: PublicKey): bool;

    toString(): string;
}
```
