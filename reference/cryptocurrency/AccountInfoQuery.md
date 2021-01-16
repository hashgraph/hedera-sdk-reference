# `AccountInfoQuery`

> class `AccountInfoQuery`
> extends [`Query`](reference/core/Query.md) <
> [`AccountInfo`](reference/cryptocurrency/AccountInfo.md) >

<details>
<summary><b>Declaration</b></summary>

```typescript
class AccountInfoQuery extends Query<AccountInfo> {
    constructor();

    /* property */ accountId: AccountId;
}
```

</details>

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

The `AccountId` for which information is requested

---
