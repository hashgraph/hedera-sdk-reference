# class `NetworkVersionInfoQuery`

Retrieve the latest state of a topic.

This method is unrestricted and allowed on any topic by any payer account.

Deleted accounts will not be returned.

Returns [`NetworkVersionInfo`](./NetworkVersionInfo.md) from [`execute`](../Query.md).

<details>
<summary><b>Declaration</b></summary>

```typescript
class NetworkVersionInfoQuery extends Query<NetworkVersionInfo> {
    constructor();
}
```

</details>

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
