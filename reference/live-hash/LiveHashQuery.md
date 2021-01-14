# class `LiveHashQuery`

Retrieve the latest state of a topic.

This method is unrestricted and allowed on any topic by any payer account.

Deleted accounts will not be returned.

Returns [`LiveHash`](./LiveHash.md) from [`execute`](../Query.md).

<details>
<summary><b>Declaration</b></summary>

```typescript
class LiveHashQuery extends Query<LiveHash> {
    constructor();

    getAccountId(): AccountId;
    setAccountId(accountId: AccountId): this;
    getHashId(): bytes;
    setAccountId(dataL bytes): this;
}
```

</details>

<!-- tabs:start -->

### ** Java **

```java
new AccountStakersQuery()
    .setAccountId(operatorId)
    .setMaxQueryPayment(new Hbar(1))
    .execute(client);
```

### ** JavaScript **

```javascript
await new LiveHashQuery()
    .setAccountId(account)
    .setNodeAccountIds([response.nodeId])
    .setHash(_hash)
    .execute(client);
```

### ** Go **

```go
_, err = NewLiveHashQuery().
    SetAccountID(accountID).
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetMaxQueryPayment(NewHbar(1)).
    SetHash(_hash).
    Execute(client)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

## Properties

### `AccountId` : [`AccountId`](reference/cryptocurrency/AccountId.md)

The Account for which information is being requested.

---

### `Hash` : `bytes`

---
