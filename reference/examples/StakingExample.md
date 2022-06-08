# Example 1: Stake hbars from an exisiting account

1. Build your client using a testnet account ID and key
2. Confgure an existing account to stake hbars to a node account (not node account ID). This will use the `AccountUpdateTransaction`
4. Show the required key used to sign the account update transaction to stake the accounts hbar i.e. the fee payer key and key to authorize changes to the account should be different
5. Return the status of the transaction to confirm it was processed and print to the console
6. Get the staking info for this the account that staked its hbar to verify
7. Print the staking response to the console
8. Use the `AccountUpdateTransaction` to unstake the account's hbars
9. Sign the transaction with the account key
10. Return the status of the transaction to confirm it was processed and print to the console
11. Get the account info to verify the hbars were unstaked
12. Print the account info results to the console


# Example 2: Create a new account and stake the account's hbars

1. Build your client using a testnet account ID and key
2. Create a new account and set the staking fields
4. Show the required key used to sign the account update transaction to stake the accounts hbar i.e. the fee payer key and key to authorize changes to the account should be different
5. Return the status of the transaction to confirm it was processed and print to the console
6. Get the staking info for this the account that staked its hbar to verify
7. Print the staking response to the console

Reference HIP: https://hips.hedera.com/hip/hip-406
