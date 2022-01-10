> abstract class `Wallet` extends `Signer`

### Static Methods

##### `withPrivateKey` ( `privateKey`: `PrivateKey` ): `Wallet`

Create a wallet using a private key

---

### Methods

##### `getProvider` (): `Provider`

Return the provider

---

##### `getPublicKey` (): `PublicKey`

Return the public key associated with this wallet.

---

##### `async createRandomED25519` (): `Wallet`

Creates a wallet with a new ED25519 key

**NOTE**: This would create an alias key account on Hedera

---

##### `async createRandomECDSA` (): `Wallet`

Creates a wallet with a new ECDSA key

**NOTE**: This would create an alias key account on Hedera

---
