# `TransactionId`

> class `TransactionId`

<details>
<summary><b>Declaration</b></summary>

```typescript
class TransactionId {
    static generate(accountId: AccountId): TransactionId;

    static fromString(text: string): TransactionId;

    constructor(accountId: AccountId, validStart: Timestamp);

    toString(): string;

    accountId: AccountId;

    validStart: Timestamp;
}
```

</details>

### Constructor

##### `constructor` ( `accountId`: `AccountId`, `validStart`: `Timestamp` )

---

### Static Methods

##### `generate` ( `accountId`: `AccountId` ): `TransactionId`

---

##### `fromString` ( `text`: `string` ): `TransactionId`

---

##### `fromBytes` ( `data`: `byte[]` ): `TransactionId`

---

### Methods

##### `toString` (): `string`

---

##### `toBytes` (): `byte[]`

---

##### `equals` (`id` : `TransactionId`): `bool`

---

##### `hashCode` (): `int`

---

### Fields

##### `accountId`: [`AccountId`](reference/AccountId.md)

---

##### `validStart`: [`Timestamp`](reference/Timestamp.md)

---
