> class `EthereumFlow`

A helper class to submit ethereum transactions to Hedera. This class will take
care of moving the call data out of the ethereum transaction into a Hedera file
if the size is too large. Current this only supports the "legacy" and EIP1559
ethereum transaction RLP formats. Other formats will error.

<!-- tabs:start -->

#### ** Java **

```java
new EthereumFlow()
    .setEthereumData(ethereumData)
    .setMaxHbarGasAllowance(new Hbar(10))
    .execute(client)
    .getReceipt(client);
```

#### ** JavaScript **

```javascript
const response = await new EthereumFlow()
    .setEthereumData(ethereumData)
    .setMaxHbarGasAllowance(new Hbar(10))
    .execute(client);

const receipt = await response.getReceipt(client);
```

#### ** Go **

```go
response, err := hedera.NewContractCreateFlow().
    SetEthereumData(ethereumData).
    SetMaxHbarGasAllowance(NewHbar(10)).
    Execute(client)
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

##### `ethereumData`: `?EthereumTransactionData`

The raw Ethereum transaction (RLP encoded type 0, 1, and 2).

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
