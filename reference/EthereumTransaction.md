> class `EthereumTransaction` extends [`Transaction`](reference/core/Transaction.md)

An Ethereum encoded transaction.
    
<!-- tabs:start -->

#### ** Java **

```java
new EthereumTransaction()
    .setEthereumData(ethereumData)
    .execute(client) // TransactionResponse
    .getReceipt(client); // TransactionReceipt
```

#### ** JavaScript **

```javascript
const transaction = new EthereumTransaction({
    ethereumData,
});

const response = await ethereumTransaction.execute(client) // TransactionResponse;
const receipt = await response.getReceipt(client) // TransactionReceipt;
```

#### ** Go **

```go
response, err := hedera.NewEthereumTransaction().
    SetEthereumData(ethereumData).
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

##### `ethereumData`: `?bytes`

The raw Ethereum transaction (RLP encoded type 0, 1, and 2). Complete 
unless the callData field is set.

---

##### `callDataFileId`: [`?FileId`](reference/file/FileId.md)

For large transactions (for example contract create) this is the callData
of the ethereumData. The data in the ethereumData will be re-written with 
the callData element as a zero length string with the original contents in 
the referenced file at time of execution. The ethereumData will need to be 
"rehydrated" with the callData for signature validation to pass.

---

##### `maxHbarGasAllowance`: [`?Hbar`](reference/Hbar.md)

The maximum amount, in tinybars, that the payer of the hedera transaction 
is willing to pay to complete the transaction.

Ordinarily the account with the ECDSA alias corresponding to the public 
key that is extracted from the ethereum\_data signature is responsible for
fees that result from the execution of the transaction. If that amount of
authorized fees is not sufficient then the payer of the transaction can be
charged, up to but not exceeding this amount. If the ethereum\_data 
transaction authorized an amount that was insufficient then the payer will
only be charged the amount needed to make up the difference. If the gas 
price in the transaction was set to zero then the payer will be assessed 
the entire fee.

---
