# `TransactionReceipt`

> class `TransactionReceipt`

<details>
<summary><b>Declaration</b></summary>

```typescript
class TransactionReceipt {
    static fromBytes(data: bytes): TransactionReceipt;

    toBytes(): bytes;

    status: Status;

    exchangeRate: ExchangeRate;

    accountId: ?AccountId;

    fileId: ?FileId;

    contractId: ?ContractId;

    topicId: ?TopicId;

    topicSequenceNumber: ?Uint64;

    topicRunningHash: ?bytes;
}
```

</details>

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): `TransactionReceipt`

---

### Methods

##### `toBytes` (): `bytes`

---

### Fields

##### `status`: `Status`

---

##### `exchangeRate`: `ExchangeRate`

---

##### `accountId`: `?AccountId`

---

##### `fileId`: `?FileId`

---

##### `contractId`: `?ContractId`

---

##### `topicId`: `?TopicId`

---

##### `topicSequenceNumber`: `Uint64`

---

##### `topicRunningHash`: `bytes`

---
