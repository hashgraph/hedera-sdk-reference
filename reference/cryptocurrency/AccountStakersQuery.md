# `AccountStakersQuery`

> class `AccountStakersQuery`
> extends [`Query`](reference/core/Query.md) <
> [`ProxyStaker[]`](reference/cryptocurrency/ProxyStaker.md) >

<details>
<summary><b>Declaration</b></summary>

```typescript
class AccountStakersQuery extends Query<ProxyStaker[]> {
    constructor();

    /* property */ accountId: AccountId;
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
