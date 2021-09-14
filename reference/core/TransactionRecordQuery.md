# `TransactionRecordQuery`

> class `TransactionRecordQuery` extends [`Query`](reference/core/Query.md) < [`TransactionRecord`](reference/core/TransactionRecord.md) >

<details>
<summary><b>Declaration</b></summary>

```typescript
class TransactionRecordQuery extends Query<TransactionRecord> {
    constructor();

    /* property */ transactionId: TransactionId;
}
```

</details>

<!-- tabs:start -->

### ** Java **

```java
var record = new TransactionRecordQuery()
    .setTransactionId(myTransactionId)
    .execute(client);
```

### ** JavaScript **

```javascript
const record = await new TransactionRecordQuery({
    transactionId: myTransactionId,
}).execute(client);
```

### ** Go **

```go
record, err := NewTransactionRecordQuery().
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
