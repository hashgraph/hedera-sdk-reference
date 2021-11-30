> class `NetworkVersionInfoQuery`
> extends [`Query`](reference/core/Query.md) <
> [`NetworkVersionInfo`](reference/network/NetworkVersionInfo.md) >

<!-- tabs:start -->

### ** Java **

```java
new NetworkVersionInfoQuery().execute(client);
```

### ** JavaScript **

```javascript
await new NetworkVersionInfoQuery()
    .setAccountId(account)
    .setNodeAccountIds([response.nodeId])
    .setHash(_hash)
    .execute(client);
```

### ** Go **

```go
_, err := NewNetworkVersionQuery().
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
