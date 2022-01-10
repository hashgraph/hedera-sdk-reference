> class `VoidSigner` extends `Signer`

### Static Methods

##### `withAccountId` ( `accountId`: `AccountId` ): `VoidSigner`

Create a wallet using a private key

---

### Methods

##### `getProvider` (): `Provider`

Return the provider

---

##### `getPublicKey` (): `PublicKey`

Will return `null`

---

##### `async signTransaction` ( `transaction`: `Transaction` )

Will do nothing

---

##### `async sendTransaction` ( `transaction`: `Transaction` ): `TransactionReceipt`

Will throw an error as sending a transaction using a `VoidSigner` is not supported.

---

