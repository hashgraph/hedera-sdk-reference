> class `AccountInfoQuery`
> extends [`Query`](reference/core/Query.md) <
> [`AccountInfo`](reference/cryptocurrency/AccountInfo.md) >

Get all the information about an account, including the balance. This does not get the list of
account records.

<!-- tabs:start -->

### ** Java **

```java
var info = new AccountInfoQuery()
    .setAccountId(accountId)
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .execute(client);
```

### ** JavaScript **

```javascript
const info = await new AccountInfoQuery()
    .setNodeAccountIds([response.nodeId])
    .setAccountId(account)
    .execute(client);
```

### ** Go **

```go
info, err := NewAccountInfoQuery().
    SetAccountID(accountID).
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
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

##### `accountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The account ID for which information is requested

---
