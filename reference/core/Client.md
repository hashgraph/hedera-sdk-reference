> class `Client`

Managed client for use on the Hedera Hashgraph network.

<!-- tabs:start -->

### ** Java **

```java
// create from..
var client = Client.forTestnet(); // pre-defined
var client = Client.fromConfigFile("./client-config.json");
var client = Client.forNetwork("mainnet", new AccountId(3)); // named
var client = Client.forName("previewnet"); // named

// set operator (to use to pay transaction fees)
client.setOperator(operatorAccountId, operatorPrivateKey);
```

### ** JavaScript **

```javascript
// create from..
const client = Client.forTestnet(); // pre-defined

const client = Client.forName("mainnet")
const client = Client.forNetwork(Network.MAINNET); // constant
const client = Client.forNetwork(Network.fromName("testnet")); // named

// set operator (to use to pay transaction fees)
client.setOperator(operatorAccountId, operatorPrivateKey);
```

### ** Go **

```go
// create from..
client := hedera.ClientForPreviewnet() // pre-defined
client := hedera.ClientForNetwork(hedera.NetworkMainnet) // constant

network, _ := hedera.NetworkFromName("mainnet")
client := hedera.ClientForNetwork(network) // named

// set operator (to use to pay transaction fees)
client.SetOperator(operatorAccountId, operatorPrivateKey)
```

### ** Python **

```python
# create from..
client = hedera.Client.for_testnet()  # pre-defined
client = hedera.Client.for_network(hedera.network.MAINNET)  # constant
client = hedera.Client.for_network(hedera.network["mainnet"])  # named

# set operator (to use to pay transaction fees)
client.set_operator(operator_account_id, operator_private_key)
```

<!-- tabs:end -->

### Static Methods

##### `forNetwork` ( `network`: `Map` < `String` , [`AccountId`](reference/core/AccountId.md) > ): `Client`

Construct a client for a specific network.

It is the responsibility of the caller to ensure that all nodes
in the map are part of the same Hedera network. Failure to do
so will result in undefined behavior.

The client will load balance all requests to Hedera using
a simple round-robin scheme to chose nodes to send transactions
to. For one transaction, at most 1/3 of the nodes will be tried.

Network constants are made available to use.

---

##### `forMainnet` (): `Client`

Construct a Hedera client pre-configured for Mainnet access.

---

##### `forTestnet` (): `Client`

Construct a Hedera client pre-configured for Testnet access.

---

##### `forPreviewnet` (): `Client`

Construct a Hedera client pre-configured for Previewnet access.

---

##### `fromConfig` ( `data`: `String` ): `Client`

Configure a client from the JSON configuration string.

<details>
<summary><b>File Specification</b></summary>

`network` can be `mainnet`, `testnet`, `previewnet`, or a dictionary of Account
ID to IP:PORT

```json
{
  "network": "mainnet",
}
```

or

```json
{
  "network": { "0.0.1": "0.testnet.hedera.com:50211" }
}
```

`operator` is an _optional_ object

```json
{
  "operator": {
    "accountId": "0.0.21",
    "privateKey": "302....",
  }
}
```

`mirrorNetwork` can be a network name (mainnet, previewnet, etc) or a list
of addresses. `mirrorNetwork` defaults to the name of `network` _if_ that is
a network name.

```json
{
  "mirrorNetwork": "mainnet",
}
```

or

```json
{
  "mirrorNetwork": [ "kabuto.sh:50211", "hedera.com:50211" ]
}
```

</details>

### Methods

---

##### `fromConfigFile` ( `filename`: `String` ): `Client`

---

##### `setOperator` ( `accountId`: [`AccountId`](reference/AccountId.md), `privateKey`: [`PrivateKey`](reference/cryptography/PrivateKey.md) ): `this`

Sets the account that will, by default, pay for transactions and queries built
with this client.

---

##### `setOperatorWith` ( `accountId`: [`AccountId`](reference/AccountId.md), `publicKey`: [`PublicKey`](reference/cryptography/PublicKey.md), `transactionSigner`: `(bytes) => bytes` ): `this`

Sets the account that will, by default, pay for transactions and queries built
with this client.

It is expected that the signing method utilize the private key associated
with the given public key.

This form is made available for integrating the SDK to sign
from an external source such as the Ledger Hardware Wallet.

---

##### `close` ()

Close all open connections with the Hedera network; and, release all
associated resources.

---

##### `ping` ()

---

##### `forName` (`name` : `String`) : `Client`

---

##### `getNetwork` () : `Map<String, AccountId>`

---

### Properties

##### `maxTransactionFee`: [`Hbar`](reference/Hbar.md)

**Write-only** The maximum fee to be paid for transactions executed by this client.

Defaults to 2 hbar.

---

##### `maxQueryPayment`: [`Hbar`](reference/Hbar.md)

**Write-only** The maximum payment allowable for queries.

Defaults to 1 hbar.

---

##### `operatorAccountId`: [`?AccountId`](reference/AccountId.md)

**Read-only**. Use `setOperator` or `setOperatorWith` to set.

---

##### `operatorPublicKey`: [`?PublicKey`](reference/cryptography/PublicKey.md)

**Read-only**. Use `setOperator` or `setOperatorWith` to set.

---

##### **Write-only** `requestTimeout`: `Duration`

---

