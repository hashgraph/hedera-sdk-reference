> class `AccountBalanceQuery`
> extends [`Query`](../core/Query.md) < [`Hbar`](../Hbar.md) >

Get the balance of a cryptocurrency account. This returns only the balance, so it is a smaller
reply than CryptoGetInfo, which returns the balance plus additional information.

> [!TIP]
> `AccountBalanceQuery` is a completely free query and does not even require
> `setOperator` to be called on the client.

<!-- tabs:start -->

#### ** Java **

```java
var balances = new AccountBalanceQuery()
    .setAccountId(operatorId)
    .execute(client);
```

#### ** JavaScript **

```javascript
const balances = await new AccountBalanceQuery()
    .setAccountId("3") // balance of node 3
    .execute(client);
```

#### ** Go **

```go
balances, err := hedera.NewAccountBalanceQuery().
    SetAccountID(client.GetOperatorAccountID()).
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

##### `accountId`: [`AccountId`](reference/AccountId.md)

The account ID for which information is requested

---

##### `contractId`: [`ContractId`](reference/ContractId.md)

The contract ID for which information is requested
