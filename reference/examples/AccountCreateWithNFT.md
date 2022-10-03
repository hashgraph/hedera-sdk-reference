# Create an account by transferring an NFT to a public key alias

This reference example is for HIP-542.

##Example 1:

### Steps
1. Create an NFT using the Hedera Token Service
2. Mint the NFT
3. Create an ECDSA public key alias
4. Tranfer the NFT to the public key alias using the transfer transaction
5. Return the new account ID in the child record
6. Show the new account ID owns the NFT

##Example 2:
1. Create a fungible HTS token using the Hedera Token Service
2. Create an ECDSA public key alias
3. Transfer the fungible token to the public key alias
4. Return the new account ID in the child record
5. Show the new account ID owns the fungible token
