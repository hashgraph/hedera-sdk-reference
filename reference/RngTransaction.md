> class `RngTransaction` extends [`Transaction`](reference/core/Transaction.md)

https://hips.hedera.com/hip/hip-351
    
<!-- tabs:start -->

#### ** Java **

```java
new RngTransaction()
    .setRange(10)
    .execute(client) // TransactionResponse
    .getReceipt(client); // TransactionReceipt
```

#### ** JavaScript **

```javascript
const transaction = new RngTransaction({
    range,
});

const response = await ethereumTransaction.execute(client) // TransactionResponse;
const receipt = await response.getReceipt(client) // TransactionReceipt;
```

#### ** Go **

```go
response, err := hedera.NewRngTransaction().
    SetRange(10).
    Execute(client) // TransactionResponse
if err != nil {
    println(err.Error())
}

receipt, err := response.GetReceipt(client)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Constructor

##### `constructor`()

---

### Properties

##### `range`: `?Uint32`

If provided and is positive, returns a 32-bit pseudorandom number from the
given range in the transaction record. If not set or set to zero, will return a
384-bit pseudorandom number in the record.

---
