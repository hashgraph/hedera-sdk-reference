> class `ProxyStaker`

Information about a single account that is proxy staking

<!-- tabs:start -->

### ** Java **

```java
var stakers = new AccountStakersQuery()
    .setAccountId(operatorId)
    .setMaxQueryPayment(new Hbar(1))
    .execute(client);

for (var staker : stakers) {
    System.out.println(staker.accountId);
    System.out.println(staker.amount);
}
```

### ** JavaScript **

```javascript
const stakers = await new AccountStakersQuery()
    .setAccountId(operatorId)
    .setMaxQueryPayment(new Hbar(1))
    .execute(client);

for (const staker of stakers) {
    console.log(staker.accountId);
    console.log(staker.amount);
}
```

### ** Go **

```go
stakers, err := NewAccountStakersQuery().
    SetAccountID(client.GetOperatorAccountID()).
    SetMaxQueryPayment(NewHbar(1)).
    Execute(client)
if err != nil {
    println(err.Error())
}

for _, staker := range stakers {
    println(staker.accountId.String());
    println(staker.amount.ToString(HbarUnits.Hbar));
}
```

<!-- tabs:end -->

### Fields

##### `accountId`: `AccountId`

The Account ID that is proxy staking

---

##### `amount`: `Hbar`

The number of hbars that are currently proxy staked

---
