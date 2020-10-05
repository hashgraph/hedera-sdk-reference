# class `Client`

<details>

<summary>Declaration</summary>

```typescript
class Client {
    static forNetwork(network: Map<string, AccountId>): Client;

    static forMainnet(): Client;
    static forTestnet(): Client;
    static forPreviewnet(): Client;

    static fromConfig(data: string): Client;
    static fromConfigFile(filename: string): Client;

    setNetwork(network: Map<string, AccountId>): this;
    setMirrorNetwork(mirrorNetwork: string[]): this;

    readonly operatorAccountId: ?AccountId;
    readonly operatorPublicKey: ?PublicKey;

    setOperator(accountId: AccountId, privateKey: PrivateKey): this;
    setOperatorWith(
        accountId: AccountId,
        publicKey: PublicKey,
        transactionSigner: (message: bytes) => bytes
    ): this;

    close();

    maxTransactionFee: Hbar;
    maxQueryPayment: Hbar;
}
```

```typescript
namespace Network {
    const MAINNET: Map<string, AccountId>;

    const TESTNET: Map<string, AccountId>;

    const PREVIEWNET: Map<string, AccountId>;
}
```

</details>

## Static Methods

### `forNetwork`

```typescript
function forNetwork(network: Map<string, AccountId>): Client;
```

Construct a client for a specific network.

It is the responsibility of the caller to ensure that all nodes
in the map are part of the same Hedera network. Failure to do
so will result in undefined behavior.

The client will load balance all requests to Hedera using
a simple round-robin scheme to chose nodes to send transactions
to. For one transaction, at most 1/3 of the nodes will be tried.

Network constants are made available to use.

### `forMainnet`

```typescript
function forMainnet(): Client;
```

Construct a Hedera client pre-configured for Mainnet access.

### `forTestnet`

```typescript
function forTestnet(): Client;
```

Construct a Hedera client pre-configured for Testnet access.

### `forPreviewnet`

```typescript
function forPreviewnet(): Client;
```

Construct a Hedera client pre-configured for Previewnet access.

### `fromConfig`

```typescript
function fromConfig(data: string): Client;
```

### `fromConfigFile`

```typescript
function fromConfigFile(filename: string): Client;
```

## Instance Methods

### `setOperator`

```typescript
function setOperator(accountId: AccountId, privateKey: PrivateKey): this;
```

### `setOperatorWith`

```typescript
function setOperatorWith(
    accountId: AccountId,
    publicKey: PublicKey,
    transactionSigner: (message: bytes) => bytes
): this;
```

Sets the account that will, by default, pay for transactions and queries built with this client.

It is expected that the signing method utilize the private key associated
with the given public key.

This form is made available for integrating the SDK to sign
from an external source such as the Ledger Hardware Wallet.

### `close`

```typescript
function close();
```

## Properties

### `maxTransactionFee`

```typescript
maxTransactionFee: Hbar;
```

Defaults to 2 hbar.

### `maxQueryPayment`

```typescript
maxQueryPayment: Hbar;
```

### `operatorAccountId`

```typescript
operatorAccountId: ?AccountId
```

**Read-only**. Use `setOperator` or `setOperatorWith` to set.

### `operatorPublicKey`

```typescript
operatorPublicKey: ?PublicKey
```

**Read-only**. Use `setOperator` or `setOperatorWith` to set.

## Examples

### JavaScript

```javascript
// create from named constructor
const client = Client.forTestnet();

// create from network constant
const client = Client.forNetwork(Network.MAINNET);
```

### Java

```java
// create from named constructor
var client = Client.forTestnet();

// create from network constant
var client = Client.forNetwork(Network.MAINNET);
```

### Go

```go
// create from named constructor
client := hedera.ClientForPreviewnet()

// create from network constant
client := hedera.ClientForNetwork(hedera.NetworkMainnet)
```

### Python

```python
# create from named constructor
client = hedera.Client.for_testnet()

# create from network constant
client = hedera.Client.for_network(hedera.network.MAINNET);
```
