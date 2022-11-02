Create an account by setting an ED25519 or ECDSA public key alias

Reference: HIP-583

## Example 1
- Create an ED25519 public key
- Create a new account using the `AccountCreateTransaction`
- Set the account public key alias by using `setAlias()` field and enter the ED25519 public key generated in the previous step
- Sign with the corresponding private key of the public key generated in the first step
- Execute the transaction
- Show the transaction was successful by asking for the receipt and returning the transaction status
- Get the new Hedera account ID from the receipt of the transaction
- Get the account info using the ED25519 public key account alias in the `AccountBalanceQuery` in the `setAccountId()` field
- Show the public key account alias is set on the account
- Show the account public key is set on the account (should be the same as the public key account alias)


## Example 2
- Create an ECDSA public key
- Create a new account using the `AccountCreateTransaction`
- Set the account public key alias by using `.setAlias()` field and enter the ECDSA public key generated in the previous step
- Sign with the corresponding private key of the public key generated in the first step
- Execute the transaction
- Show the transaction was successful by asking for the receipt and returning the transaction status
- Get the new Hedera account ID from the receipt of the transaction
- Get the account info using the ECDSA public key account alias in the `AccountBalanceQuery`
- Show the public key account alias is set on the account
- Show the account public key is set on the account (should be the same as the public key account alias)
