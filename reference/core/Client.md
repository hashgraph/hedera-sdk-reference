> class `Client`

Managed client for use on the Hedera Hashgraph network.

<!-- tabs:start -->

### ** Java **

```java
// create from..
var network = new HashMap<String, AccountId>();
network.put("0.testnet.hedera.com:50211", new AccountId(3));

var client = Client.forMainnet(); // pre-defined
var client = Client.forNetwork(newtork); // custom network
var client = Client.fromConfigFile("./client-config.json"); // configuration file
var client = Client.forName("testnet"); // named

// set operator (to use to pay transaction fees)
client.setOperator(operatorAccountId, operatorPrivateKey);
```

### ** JavaScript **

```javascript
// create from..
const network = {
    "0.testnet.hedera.com:50211": "0.0.3"
};

var client = Client.forMainnet(); // pre-defined
var client = Client.forNetwork(newtork); // custom network
var client = Client.fromConfigFile("./client-config.json"); // configuration file
var client = Client.forName("testnet"); // named

// set operator (to use to pay transaction fees)
client.setOperator(operatorAccountId, operatorPrivateKey);
```

### ** Go **

```go
// create from..
network := make(map[string]AccountID)
newtork["0.testnet.hedera.com:50211"] = AccountID{Account: 3}

client := ClientForMainnet(); // pre-defined
client := ClientForNetwork(newtork); // custom network
client, err := ClientFromConfigFile("./client-config.json"); // configuration file
client, err := ClientForName("testnet"); // named

// set operator (to use to pay transaction fees)
client.setOperator(operatorAccountId, operatorPrivateKey);
```

<!-- tabs:end -->

### Static Methods

##### `forNetwork` ( `network`: `Map` < `String` , [`AccountId`](reference/cryptocurrency/AccountId.md) > ): `Client`

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

##### `forName` ( `name`: `String` ): `Client`

Construct a Hedera client for a given name.

Valid names are "previewnet", "testnet", "mainnet"

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

##### `setOperator` ( `accountId`: [`AccountId`](reference/cryptocurrency/AccountId.md), `privateKey`: [`PrivateKey`](reference/cryptography/PrivateKey.md) ): `Client`

Sets the account that will, by default, pay for transactions and queries built
with this client.

---

##### `setOperatorWith` ( `accountId`: [`AccountId`](reference/cryptocurrency/AccountId.md), `publicKey`: [`PublicKey`](reference/cryptography/PublicKey.md), `transactionSigner`: `(bytes) => bytes` ): `Client`

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

##### `ping` ( `nodeAccountId`: [`AccountId`](reference/cryptocurrency/AccountId.md))

Ping a single node

**NOTE**: This method will **not** throw if the node doesn't respond with a successful status code,
instead the network will de-prioritize it.

---

##### `pingAll` ()

Ping all nodes in the current network.

**NOTE**: This method will **not** throw if a node doesn't respond with a successful status code,
instead the network will de-prioritize it.

---

### Properties

##### `network` () : `Map` < `String` , [`AccountId`](reference/cryptocurrency/AccountId.md) >

---

##### `mirrorNetwork` () : `List` < `String` >

---

##### `defaultMaxTransactionFee`: [`Hbar`](reference/Hbar.md)

**Write-only** The maximum fee to be paid for transactions executed by this client.

Defaults to 2 hbar.

---

##### `defaultMaxQueryPayment`: [`Hbar`](reference/Hbar.md)

**Write-only** The maximum payment allowable for queries.

Defaults to 1 hbar.

---

##### `operatorAccountId`: [`?AccountId`](reference/cryptocurrency/AccountId.md)

**Read-only**. Use `setOperator` or `setOperatorWith` to set.

---

##### `operatorPublicKey`: [`?PublicKey`](reference/cryptography/PublicKey.md)

**Read-only**. Use `setOperator` or `setOperatorWith` to set.

---

##### `requestTimeout`: `Duration`

---

##### `transportSecurity` () : `bool`

Enable or disable TLS for both networks.

---

##### `verifyCertificates` () : `bool`

Enable or disable TLS certificate verification

Only available in Java and Go SDKs 

---

##### `ledgerId` () : [`LedgerId`](reference/LedgerId.md)

Enable or disable TLS certificate verification

Only available in Java and Go SDKs 

---

