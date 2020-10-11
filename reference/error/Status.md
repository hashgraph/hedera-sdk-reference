# `Status`

> error `Status`

<details>
<summary><b>Declaration</b></summary>

```typescript
class StatusError extends Error {
    readonly status: Status;
    readonly transactionId: ?TransactionId;
}
```

</details>

- Each language has differing naming conventions for errors:
  - Java, Dart — `StatusException`
  - Rust, JavaScript, Python — `StatusError`
  - Go — `ErrStatus`
  - C — `HEDERA_ERR_STATUS`, etc.

### Derived

- [`PrecheckStatus`](reference/error/PrecheckStatus.md)
- [`ReceiptStatus`](reference/error/ReceiptStatus.md)

### Fields

##### `status`: [`Status`](reference/Status.md)

---

##### `transactionId`: [`?TransactionId`](reference/core/TransactionId.md)

---
