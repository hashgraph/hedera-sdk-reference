> class `LiveHashQuery` extends [`Query`](reference/core/Query.md) < [`LiveHash`](reference/contract/ContractInfo.md) >

Returns the full livehash associated to an account, if it is present. Note that the only way to
obtain a state proof exhibiting the absence of a livehash from an account is to retrieve a state
proof of the entire account with its list of livehashes.

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

### Constructor

##### `constructor`()

---

## Properties

### `accountId` : [`AccountId`](reference/cryptocurrency/AccountId.md)

The Account for which information is being requested.

---

### `hash` : `bytes`

---
