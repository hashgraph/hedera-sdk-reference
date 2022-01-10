> `LocalWallet` implements `Wallet`

### Static Methods

### Constructor

##### `constructor`()

Creates an `LocalWallet` from the environment variables `OPERATOR_KEY`, `OPERATOR_ID`, and `HEDERA_NEWTORK`

---

### Methods

##### async `sign` ( `messages`: `List` < `bytes` > ): `List` < `List` < `SignatureProviderSignature` > >

Signs all the messages with all the private keys.

---
