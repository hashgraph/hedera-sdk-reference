> class `TransactionRecord`

Response when the client sends the node TransactionGetRecordResponse

### Static Methods

##### `fromBytes` ( `data`: `byte[]` ): `TransactionRecord`

Decode a `TransactionRecord` from an appropriate protobuf encode structure

---

### Methods

##### `toBytes` (): `byte[]`

The byte representation of the encoded protobuf type

---

##### `toString` (): `String`

Stringification of all the current values

---

### Fields

### `aliasKey`: [`PublicKey`](../cryptography/PublicKey.md)

In the record of an internal CryptoCreate transaction triggered by a user transaction with a
(previously unused) alias, the new account's alias.

---

### `assessedCustomFees`: `List` < [`AssessedCustomFee`](../token/AssessedCustomFee.md) >

In the record of an internal transaction, the consensus timestamp of the user transaction that spawned it.

---

### `automaticTokenAssociations`: `List` < [`TokenAssociation`](../token/TokenAssociation.md) >

In the record of an internal transaction, the consensus timestamp of the user transaction that spawned it.

---

### `children`: [`TransactionRecord`](TransactionRecord.md)

The records of processing all child transaction spawned by the transaction with the given
top-level id, in consensus order. Always empty if the top-level status is UNKNOWN.

---

### `consensusTimestamp`: `Timestamp`

The timestamp the transaction came to consensus

---

### `contractFunctionResult`: [`?ContractFunctionResult`](../contract/ContractFunctionResult.md)

Result of a [`ContractExecuteTransaction`](../contract/ContractExecuteTransaction.md)

---

### `duplicates`: [`TransactionRecord`](TransactionRecord.md)

The records of processing all consensus transaction with the same id as the distinguished
record above, in chronological order.

---

### `ethereumHash`: `Bytes`

The keccak256 hash of the ethereumData.

**NOTE**: This field will only be populated for EthereumTransaction.

---

### `evmAddress`: `Bytes`

The EOA 20-byte address to create that is derived from the keccak-256 hash of a ECDSA_SECP256K1 primitive key.

---

### `paidStakingRewards`: [`Transfer`](../Transfer.md)

List of accounts with the corresponding staking rewards paid as a result of a transaction.

---

### `parentConsensusTimestamp`: `Timestamp`

In the record of an internal transaction, the consensus timestamp of the user transaction that spawned it.

---

### `prngBytes`: `Bytes`

In the record of a UtilPrng transaction with no output range, a pseudorandom 384-bit string.

---

### `prngNumber`: `Uint32`

In the record of a PRNG transaction with an output range, the output of a PRNG whose input was a 384-bit string.

---

### `receipt`: [`TransactionReceipt`](TransactionReceipt.md)

Receipt for the transaction

---

### `scheduleRef`: [`ScheduleId`](../schedule/ScheduleId.md)

In the record of an internal transaction, the consensus timestamp of the user transaction that spawned it.

---

### `tokenNftTransfers`: `Map` < [`TokenId`](../token/TokenId), `List` < `TokenNftTransfer`>>

All NFT Token transfers as a result of this transaction

---

### `tokenTransferList`: `List` < `TokenTransfer` >

All fungible token transfers as a result of this transaction as a list

---

### `tokenTransfers`: `Map` < [`TokenId`](../token/TokenId), `Map` < [`AccountId`](../cryptocurrency/AccountId.md), `Uint64`>>

Any token transfers made in this transaction

**Note**: These token transfers are different from the ones set in [`TransferTransaction`](../cryptocurrency/TransferTransaction.md)

---

### `transactionFee`: [`Hbar`](../Hbar.md)

Fee set on the transaction

---

### `transactionHash`: `bytes`

Hash of the transaction

---

### `transactionId`: [`TransactionId`](TransactionId.md)

Transaction ID of the transaction

---

### `transactionMemo`: `String`

Memo set on the transaction

---

### `transfers`: [`Transfer[]`](../Transfer.md)

Any transfers made in this transaction

**Note**: Includes fee payments
