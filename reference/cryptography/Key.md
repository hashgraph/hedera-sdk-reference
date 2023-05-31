> interface `Key`

A Key can be a public key from one of the three supported systems (ed25519, RSA-3072,  ECDSA with
p384). Or, it can be the ID of a smart contract instance, which is authorized to act as if it had
a key. If an account has an ed25519 key associated with it, then the corresponding private key
must sign any transaction to transfer cryptocurrency out of it. And similarly for RSA and ECDSA.

A Key can be a smart contract ID, which means that smart contract is to authorize operations as
if it had signed with a key that it owned. The smart contract doesn't actually have a key, and
doesn't actually sign a transaction. But it's as if a virtual transaction were created, and the
smart contract signed it with a private key.

A Key can be a "threshold key", which means a list of M keys, any N of which must sign in order
for the threshold signature to be considered valid. The keys within a threshold signature may
themselves be threshold signatures, to allow complex signature requirements.

A Key can be a "key list" where all keys in the list must sign unless specified otherwise in the
documentation for a specific transaction type (e.g.  FileDeleteTransactionBody).  Their use is
dependent on context. For example, a Hedera file is created with a list of keys, where all of
them must sign a transaction to create or modify the file, but only one of them is needed to sign
a transaction to delete the file. So it's a single list that sometimes acts as a 1-of-M threshold
key, and sometimes acts as an M-of-M threshold key.  A key list is always an M-of-M, unless
specified otherwise in documentation. A key list can have nested key lists or threshold keys.
Nested key lists are always M-of-M. A key list can have repeated Ed25519 public keys, but all
repeated keys are only required to sign once.

A Key can contain a ThresholdKey or KeyList, which in turn contain a Key, so this mutual
recursion would allow nesting arbitrarily deep. A ThresholdKey which contains a list of primitive
keys (e.g., ed25519) has 3 levels: ThresholdKey -> KeyList -> Key. A KeyList which contains
several primitive keys (e.g., ed25519) has 2 levels: KeyList -> Key. A Key with 2 levels of
nested ThresholdKeys has 7 levels: Key -> ThresholdKey -> KeyList -> Key -> ThresholdKey ->
KeyList -> Key.

Each Key should not have more than 46 levels, which implies 15 levels of nested ThresholdKeys.
Only ed25519 primitive keys are currently supported.

**Note**: [`ContractId`](../contract/ContractId.md) can represent either a regular
contract ID or a delegatable contract ID.

### Implementors

- [`PublicKey`](../cryptography/PublicKey.md)
- [`PrivateKey`](../cryptography/PrivateKey.md)
- [`KeyList`](../cryptography/KeyList.md)
- [`ContractId`](../contract/ContractId.md)
