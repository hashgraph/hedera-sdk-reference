> class `AccountRecordsQuery`
> extends [`Query`](../core/Query.md) <
> [`TransactionRecord[]`](../core/TransactionRecord.md) >

Request records of all transactions for which the given account was the
effective payer in the last 3 minutes of consensus time and
<tt>ledger.keepRecordsInState=true</tt> was true during
<tt>handleTransaction</tt>.

<!-- tabs:start -->

### ** Java **

```java
var records = new AccountRecordsQuery()
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .setAccountId(accountId)
    .execute(client);
```

### ** JavaScript **

```javascript
const records = await new AccountRecordsQuery()
    .setNodeAccountIds([response.nodeId])
    .setAccountId(operatorId)
    .execute(client);
```

### ** Go **

```go
recordsQuery, err := NewAccountRecordsQuery().
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetAccountID(client.GetOperatorAccountID()).
    SetMaxQueryPayment(NewHbar(1)).
    Execute(client)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Constructor

##### `constructor`()

---

### Properties

##### `accountId`: [`AccountId`](AccountId.md)

The account ID for which the records should be retrieved
