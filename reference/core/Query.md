# `Query`

> abstract class `Query<O>`

<details>
<summary><b>Declaration</b></summary>

```typescript
abstract class Query<O> {
    static fromBytes(data: bytes): Query<*>;

    /* property */ nodeAccountId: AccountId;

    /* property */ queryPayment: ?Hbar;

    /* property */ maxQueryPayment: ?Hbar;

    toBytes(): bytes;

    getCost(client: Client): Hbar;

    execute(client: Client): O;
}
```

</details>

Base class for all queries that may be submitted to Hedera.

### Static Methods

##### `fromBytes` ( `data` : `bytes` ): `Query<*>`

---

### Methods

##### `execute` ( `client`: `Client` ): `O`

Execute this query on the chosen Hedera network node and return its response.

The return type of this method is dictated by the derived class.

---

##### `getCost` ( `client`: `Client` ): `Hbar`

Return the cost to execute this query on the chosen Hedera network node.

---

##### `toBytes` (): `bytes`

Encodes this query to a byte array that can be later decoded into the same `Query`.

---

### Properties

##### `nodeAccountId`: [`AccountId`](reference/AccountId.md)

The account ID of the node that this query will be submitted to.

---

##### `maxQueryPayment`: [`?Hbar`](reference/Hbar.md)

The maximum query payment the client is willing to pay.

Defaults to `maxQueryPayment` from the `client`.

---

##### `queryPayment`: [`?Hbar`](reference/Hbar.md)

The exact query payment the client will pay for this query.

If not set, the cost will be dynamically fetched from the network and used (
respecting the `maxQueryPayment` setting).

---
