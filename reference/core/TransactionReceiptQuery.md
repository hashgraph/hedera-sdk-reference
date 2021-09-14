# `TransactionReceiptQuery`

> class `TransactionReceiptQuery` extends [`Query`](reference/core/Query.md) < [`TransactionReceipt`](reference/core/TransactionReceipt.md) >

<details>
<summary><b>Declaration</b></summary>

```typescript
class TransactionReceiptQuery extends Query<TransactionReceipt> {
    constructor();

    /* property */ transactionId: TransactionId;
}
```

</details>

<!-- tabs:start -->

### ** Java **

```java
var receipt = new TransactionReceiptQuery()
    .setTransactionId(myTransactionId)
    .execute(client);
```

### ** JavaScript **

```javascript
const receipt = await new TransactionReceiptQuery({
    transactionId: myTransactionId,
}).execute(client);
```

### ** Go **

```go
receipt, err := NewTransactionReceiptQuery().
    SetTransactionID(response.TransactionID).
    SetNodeAccountIDs([]AccountID{response.NodeID}).
    Execute(client)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Constructor

##### `constructor` ()

---

### Properties

##### `transactionId`: `TransactionId`

---
