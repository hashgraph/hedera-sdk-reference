# `TokenApproval`

## Properties

##### `tokenId`: [`TokenId`](reference/token/TokenId.md)

The token that the allowance pertains to.

---

##### `spenderAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The account ID of the spender of the hbar allowance.

---

##### `amount`: `Uint64?`

The amount of the spender's token allowance.

**NOTE**: If `null`, the spender has access to all of the account owner's NFT instances (currently
owned and any in the future).

---
