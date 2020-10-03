# class `PrivateKey`

## Static Methods

### `generate(): PrivateKey`

### `fromString(text: string): PrivateKey`

### `fromMnemonic(mnemonic: string, passphrase: string): PrivateKey`

Recovers an ed25519 private key from a 24, 22, or 12 word mnemonic. 24 and
12 word mnemonics use a BIP-32 word list and SLIP-10 deriviation. 22 word
mnemonics use a legacy word list from the original Hedera mobile wallets.

#### Errors

 * [`BadMnemonic`](./BadMnemonic.md) — when the mnemonic contains words not found in the word list; there is a checksum mismatch; or, an unexpected number of words.

#### Examples

###### Java

```java
// use "" for an empty passphrase
var key = PrivateKey.fromMnemonic("word,word2,word3", "");
```

###### Go

```go
key, _ := PrivateKeyFromMnemonic("word1,word2,word3", "");
```

### `fromPem(data: string, passphrase: string): PrivateKey`

### `fromKeystore(data: bytes, passphrase: string): PrivateKey`

## Methods

### `isDerivable(): boolean`

### `derive(index: int): PrivateKey`

### `sign(message: bytes): bytes`

### `toString(): string`

### `toKeystore(passphrase: string): bytes`

## Properties

### `publicKey: PublicKey`

## Declaration

```typescript
class PrivateKey implements Key {
    static generate(): PrivateKey;

    static fromString(text: string): PrivateKey;

    static fromMnemonic(mnemonic: string, passphrase: string): PrivateKey;

    static fromKeystore(data: bytes, passphrase: string): PrivateKey;

    static fromPem(text: string, passphrase: string): PrivateKey;

    isDerivable(): bool;

    derive(index: int): PrivateKey;

    getPublicKey(): PublicKey;

    sign(message: bytes): bytes;

    toString(): string;

    toKeystore(passphrase: string): bytes;
}
```
