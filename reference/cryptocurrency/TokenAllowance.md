
# `TokenAllowance`

## Properties

##### `tokenId`: [`TokenId`](reference/token/TokenId.md)

The token that the allowance pertains to.

---

##### `spenderAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The account ID of the spender of the hbar allowance.

---

##### `amount`: `Uint64?`

The current balance of the spender's token allowance.

**NOTE**: If `null`, the spender has access to all of the account owner's NFT instances (currently
owned and any in the future).

---

##### `decimals`: `Int32`

The number of decimal places the token allowance value is divisible by.

---
