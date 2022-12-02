Create an account and set a public key alias. 

Reference: [HIP-583 Expand alias support in CryptoCreate & CryptoTransfer Transactions](https://hips.hedera.com/hip/hip-583)

## Example 1:
- Create an ECDSA private key
- Get the ECDSA public key 
- Use the `AccountCreateTransaction` and populate the `setAlias(<ECDSA_public_key)` field
- Sign the `AccountCreateTransaction` using an existing Hedera account and key to pay for the transaction fee
- Execute the transaction
- Return the Hedera account ID from the receipt of the transaction
- Get the `AccountInfo` using the new account ID
- Get the `AccountInfo` using the account public key in `0.0.aliasPublicKey` format
- Show the public key and the public key alias are the same on the account
- Show this account has a corresponding EVM address in the mirror node



## Example 2:
- Create an EDD2519 private key
- Get the EDD2519 public key 
- Use the `AccountCreateTransaction` and populate the `setAlias(<ECDSA_public_key)` field
- Sign the `AccountCreateTransaction` using an existing Hedera account and key to pay for the transaction fee
- Execute the transaction
- Return the Hedera account ID from the receipt of the transaction
- Get the `AccountInfo` using the new account ID
- Get the `AccountInfo` using the account public key in `0.0.aliasPublicKey` format
- Show the public key and the public key alias are the same on the account
- Show this account has a corresponding EVM address in the mirror node
