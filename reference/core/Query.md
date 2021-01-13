# `Query`

> abstract class `Query<O>`

<details>
<summary><b>Declaration</b></summary>

```typescript
abstract class Query<O> {
    /* property */ nodeAccountIds: AccountId[];

    /* property */ maxQueryPayment: ?Hbar;

    /* property */ queryPayment: ?Hbar;

    execute(client: Client): O;

    getCost(client: Client): Hbar;
}
```

</details>

<details>
<summary><b>Table of Contents</b></summary>



| Item | Java | JavaScript | Go
| - | - | - | - |
| [`execute`](#execute-client-client-o) | ✅ | ✅ | ✅
| [`getCost`](#getcost-client-client-hbar) | ✅ | ✅ | ✅
| [`nodeAccountIds`](#nodeaccountids-accountId) | ✅ | ✅ | ✅
| [`maxQueryPayment`](#write-only-maxquerypayment-hbar) | ✅ | ✅ | ✅
| [`queryPayment`](#write-only-querypayment-hbar) | ✅ | ✅ | ✅

</details>

Base class for all queries that may be submitted to Hedera.

### Methods

##### `execute` ( `client`: [`Client`](reference/core/Client.md) ): `O`

Execute this query on the chosen Hedera network node and return its response.

The return type of this method is dictated by the derived class.

---

##### `getCost` ( `client`: [`Client`](reference/core/Client.md) ): [`Hbar`](reference/Hbar.md)

Return the cost to execute this query on the chosen Hedera network node.

---

### Properties

##### `nodeAccountIds`: [`AccountId[]`](reference/cryptocurrency/AccountId.md)

The nodeaccount IDs that will be queried.

---

##### **Write-only** `maxQueryPayment`: [`?Hbar`](reference/Hbar.md)

The maximum query payment the client is willing to pay.

Defaults to `maxQueryPayment` from the `client`.

---

##### **Write-only** `queryPayment`: [`?Hbar`](reference/Hbar.md)

The exact query payment the client will pay for this query.

If not set, the cost will be dynamically fetched from the network and used (
respecting the `maxQueryPayment` setting).

---
