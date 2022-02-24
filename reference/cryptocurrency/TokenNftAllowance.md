# `TokenNftAllowance`

## Properties

##### `ownerAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The account ID of the hbar owner (ie. the grantor of the allowance).

##### `tokenId`: [`TokenId`](reference/token/TokenId.md)

The token that the allowance pertains to.

---

##### `spenderAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The account ID of the spender of the hbar allowance.

---

##### `serialNumbers`: `List` < `Uint64` > `?`

The current balance of the spender's token allowance.

**NOTE**: If `null`, the spender has access to all of the account owner's NFT instances
(currently owned and any in the future).

---
