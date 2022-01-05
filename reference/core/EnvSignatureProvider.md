> `EnvSignatureProvider` implements `SignatureProvider`

### Static Methods

##### `fromVariables` ( `variable`: `List` < `string` > ): `EnvSignatureProvider`

Creates an `EnvSignatureProvider` from a list of environment variable

---

##### `fromDefault` (): `EnvSignatureProvider`

Creates an `EnvSignatureProvider` from the default environment variable `OPERATOR_KEY`

---

### Methods

##### async `getPublicKeys` (): `List` < `PublicKey` >

Returns the public keys of all the private keys which will sign requests

##### async `sign` ( `messages`: `List` < `bytes` > ): `List` < `List` < `SignatureProviderSignature` > >

Signs all the messages with all the private keys.

---

##### `toString` (): `string`

Outputs `[EnvSignatureProvider] <public_key>`

---
