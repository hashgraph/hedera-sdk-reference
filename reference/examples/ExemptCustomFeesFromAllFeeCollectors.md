# Create a token that exempts all custom fees for all accounts in the custom fee list

This examples HIP-573: Blanket exemptions for custom fee collectors

1. Create a token that has the feature to exempt all collectors from being charged a custom fee set to true
2. Create an account to transfer the token to
3. Transfer the token to that account
4. Get the transaction fee for that transfer transaction
5. Show that the fee collector account in the custom fee list of the token that was created was not charged a custom fee in the transfer
