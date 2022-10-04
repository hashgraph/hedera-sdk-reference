# Create a token that exempts all custom fees for all accounts in the custom fee list

This examples HIP-573: Blanket exemptions for custom fee collectors

1. Create accounts A, B, and C
2. Create a fungible token that has three fractional fees
Fee #1 sends 1/100 of the transferred value to collector 0.0.A.
Fee #2 sends 2/100 of the transferred value to collector 0.0.B.
Fee #3 sends 3/100 of the transferred value to collector 0.0.C.
3. Collector 0.0.B sends 10_000 units of the token to 0.0.A.
4. Get the transaction fee for that transfer transaction
5. Show that the fee collector accounts in the custom fee list of the token that was created was not charged a custom fee in the transfer
