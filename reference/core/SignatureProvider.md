> interface `SignatureProvider`

### Methods

##### async `getPublicKeys` (): `List` < `PublicKey` >

List all the public keys that will sign the requests

Still on the fence of if this type of method is really necessary, but it can be helpful
for determining if mutliple providers have the same public key.

##### async `sign` ( `messages`: `List` < `bytes` > ): `List` < `List` < `SignatureProviderSignature` > >

Sign a list of messages

**NOTE**: Each element in the outer list of the result is all the signatures for the
at the same index.

---

##### `toString` (): `string`

Ouput should match `[(?<provider_name>:\w+] .*`

---
