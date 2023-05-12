> class `TransactionReceiptQuery` extends [`Query`](Query.md) < [`TransactionReceipt`](TransactionReceipt.md) >

Get the receipt of a transaction, given its transaction ID.
<br>
Once a transaction reaches consensus, then information about whether it succeeded or failed will be available until the end of the receipt period.
<br>
This query is free.

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

##### `includeDuplicates`: `bool`

Whether receipts of processing duplicate transactions should be returned along with the
receipt of processing the first consensus transaction with the given id whose status was
neither <tt>INVALID\_NODE\_ACCOUNT</tt> nor <tt>INVALID\_PAYER\_SIGNATURE</tt>; <b>or</b>, if no
such receipt exists, the receipt of processing the first transaction to reach consensus with
the given transaction id.

---

##### `includeChildren`: `bool`

Whether the response should include the receipts of any child transactions spawned by the
top-level transaction with the given transactionID.

---

##### `transactionId`: [`TransactionId`](TransactionId.md)

The transaction ID to query the receipt for
