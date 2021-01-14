# `TokenInfoQuery`

> class `TokenInfoQuery`
> extends [`Query`](reference/core/Query.md) <
> [`TokenInfo`](reference/token/TokenInfo.md) >

<details>
<summary><b>Declaration</b></summary>

```typescript
class TokenInfoQuery extends Query<TokenInfo> {
    constructor();

    /* property */ TokenId: TokenId;
}
```

</details>

<!-- tabs:start -->

### ** Java **

```java
 var info = new TokenInfoQuery()
    .setNodeAccountIds(Collections.singletonList(response.nodeId))
    .setTokenId(tokenId)
    .execute(client);
```

### ** JavaScript **

```javascript
const info = await new TokenInfoQuery()
    .setNodeAccountIds([response.nodeId])
    .setTokenId(tokenId)
    .execute(client);
```

### ** Go **

```go
info, err := NewTokenInfoQuery().
    SetNodeAccountIDs([]AccountID{resp.NodeID}).
    SetTokenID(tokenID).
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

##### `tokenId`: `TokenId`

---
