# 1. Create and submit a schedule transaction for the future

1. Create a Hedera client using credentials provided by the Hedera portal
2. Create an account to transfer to with some hbars and 2 keys
3. Create a transfer transaction between two accounts (the account created in the previous line to the account associated with the client)
4. Create a schedule transaction and schedule the transfer transaction and set the expiration time to 24 hours into the future and wait for expiry to true
5. Get the record and log the schedule transaction ID as well as the transaction ID of that was scheduled
7. Create a schedule sign transaction and submit one of the signatures
8. Get the schedule info of the schedule transaction to view the applied signatures
9. Create a schedule sign transaction and submit a second signature
10.Get the schedule info of the schedule transaction to view the applied signatures
11. Get the schedule info query to verify the schedule transaction was triggered
12. Query the mirror node with the schedule transaction ID to get the record of it executing
