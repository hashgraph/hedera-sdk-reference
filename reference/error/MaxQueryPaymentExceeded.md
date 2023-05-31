> class `MaxQueryPaymentExceeded` extends `Error`

Signals that a query will cost more than a pre-configured maximum payment amount.

### Fields

##### `maxQueryPayment`: [`Hbar`](../Hbar.md)

The limit for a single automatic query payment, set by
[`Client.setMaxQueryPayment(Hbar)`](../core/Client.md#defaultmaxquerypayment--hbar) or [`Query.setMaxQueryPayment(Hbar)`](../core/Query.md#write-only-maxquerypayment--hbar).

---

##### `queryCost`: [`Hbar`](../Hbar.md)

The cost of the query that was attempted as returned by [`Query.getCost`](../core/Query.md#getcost--client--client---hbar)
