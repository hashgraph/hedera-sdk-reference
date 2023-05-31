> class `TransactionRecordQuery` extends [`Query`](Query.md) < [`TransactionRecord`](TransactionRecord.md) >

Get the record for a transaction.

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

##### `includeChildren`: `bool`

Whether the response should include the records of any child transactions spawned by the
top-level transaction with the given transactionID.

---

##### `includeDuplicates`: `bool`

Whether records of processing duplicate transactions should be returned along with the record
of processing the first consensus transaction with the given id whose status was neither
<tt>INVALID\_NODE\_ACCOUNT</tt> nor <tt>INVALID\_PAYER\_SIGNATURE</tt>; <b>or</b>, if no such
record exists, the record of processing the first transaction to reach consensus with the
given transaction id..

---

##### `transactionId`: [`TransactionId`](TransactionId.md)

The transaction ID to query the record for
