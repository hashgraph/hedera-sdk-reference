> class `MaxQueryPaymentExceeded` extends `Error`

### Fields

##### `queryCost`: [`Hbar`](reference/Hbar.md)

The cost of the query that was attempted as returned by [`Query.getCost`](reference/core/Query.md#getcost-client-client-hbar)

---

##### `maxQueryPayment`: [`Hbar`](reference/Hbar.md)

The limit for a single automatic query payment, set by
[`Client.setMaxQueryPayment(Hbar)`](reference/core/Client.md#maxquerypayment-hbar) or [`Query.setMaxQueryPayment(Hbar)`](reference/core/Query.md#write-only-maxquerypayment-hbar).

---
