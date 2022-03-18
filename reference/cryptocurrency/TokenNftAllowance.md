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

---

##### `allSerials`: `boolean?`

A `true` value indicates that this allowance pertains to all serial numbers.

In the context of a [`AccountAllowanceAdjustTransaction`](reference/cryptocurrency/AccountAllowanceAdjustTransaction.md), a `false` value (in contrast to `null`) indicates that allowances for all serial numbers shall be _revoked_.

---
