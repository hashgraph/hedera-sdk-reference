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

    topicSupply: ?Uint64;
}
```

</details>

### Static Methods

##### `fromBytes` ( `data`: `bytes` ): `TransactionReceipt`

---

### Methods

##### `toBytes` (): `bytes`

---

##### `toString` (): `String`

---

### Fields

##### `status`: [`Status`](reference/Status.md)

---

##### `exchangeRate`: [`ExchangeRate`](reference/ExchangeRate.md)

---

##### `accountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

---

##### `fileId`: [`FileID`](reference/file/FileId.md)

---

##### `contractId`: [`ContractId`](reference/contract/ContractId.md)

---

##### `topicId`: [`TopicId`](reference/consensus/TopicId.md)

---

##### `TokenId`: [`TokenId`](reference/token/TokenId.md)

---

##### `topicSequenceNumber`: `Uint64`

---

##### `topicRunningHash`: `bytes`

---

##### `totalSypply`: `Uint64`

---
