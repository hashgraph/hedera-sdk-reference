# `AccountStakersQuery`

> class `AccountStakersQuery`
> extends [`Query`](reference/core/Query.md) <
> [`ProxyStaker[]`](reference/cryptocurrency/ProxyStaker.md) >

Get all the accounts that are proxy staking to this account. For each of them, give the amount
currently staked. This is not yet implemented, but will be in a future version of the API.

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
await new AccountStakersQuery()
    .setAccountId(operatorId)
    .setMaxQueryPayment(new Hbar(1))
    .execute(client);
```

### ** Go **

```go
_, err := NewAccountStakersQuery().
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

##### `accountId`: [`AccountId`](reference/cryptocurrency/AccountId.md)

The `AccountId` for which the records should be retrieved

---
