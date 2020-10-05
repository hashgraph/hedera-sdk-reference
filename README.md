# Hedera™ Hashgraph SDK Reference

![Hedera Hasgraph](https://www.hedera.com/logo-capital-hbar-wordmark.jpg)

This document is the primary reference for the Hedera™ Hashgraph SDKs.

This document is normative and should be taken as the official specification for
semantic operation and classification of an **Official** Hedera™ Hashgraph SDK.

## Reference

### Cryptography

* [interface `Key`](reference/cryptography/Key.md)

* [class `KeyList`](reference/cryptography/KeyList.md)

* [class `PrivateKey`](reference/cryptography/PrivateKey.md)

* [class `PublicKey`](reference/cryptography/PublicKey.md)

* [class `Mnemonic`](reference/cryptography/Mnemonic.md)

* [error `BadKey`](reference/cryptography/BadKey.md)

* [error `BadMnemonic`](reference/cryptography/BadMnemonic.md)

* [enum `BadMnemonicReason`](reference/cryptography/BadMnemonicReason.md)

### Client

* [`Client`] – The protocol wrapper for the SDK, used by all transaction
    and query types. A `Client` is established to one network (with one
    or more nodes) and an optional operator account and key (to sign
    transactions).

### Transactions

* [`CryptoTransferTransaction`](reference/CryptoTransferTransaction.md)

#### Account Transactions

* [`AccountCreateTransaction`](reference/AccountCreateTransaction.md)

* [`AccountUpdateTransaction`](reference/AccountUpdateTransaction.md)

* [`AccountDeleteTransaction`](reference/AccountDeleteTransaction.md)

#### Contract Transactions

* [`ContractCreateTransaction`](reference/ContractCreateTransaction.md)

* [`ContractUpdateTransaction`](reference/ContractUpdateTransaction.md)

* [`ContractDeleteTransaction`](reference/ContractDeleteTransaction.md)

* [`ContractExecuteTransaction`](reference/ContractExecuteTransaction.md)

#### File Transactions

* [`FileCreateTransaction`](reference/FileCreateTransaction.md)

* [`FileAppendTransaction`](reference/FileAppendTransaction.md)

* [`FileUpdateTransaction`](reference/FileUpdateTransaction.md)

* [`FileDeleteTransaction`](reference/FileDeleteTransaction.md)

#### Topic Transactions

* [`TopicCreateTransaction`](reference/TopicCreateTransaction.md)

* [`TopicUpdateTransaction`](reference/TopicUpdateTransaction.md)

* [`TopicDeleteTransaction`](reference/TopicDeleteTransaction.md)

* [`TopicMessageSubmitTransaction`](reference/TopicMessageSubmitTransaction.md)

#### System Transactions

* [`SystemDeleteTransaction`](reference/SystemDeleteTransaction.md)

* [`SystemUndeleteTransaction`](reference/SystemUndeleteTransaction.md)

* [`FreezeTransaction`](reference/FreezeTransaction.md)

### Queries

* [`TransactionReceiptQuery`](reference/TransactionReceiptQuery.md)

* [`TransactionRecordQuery`](reference/TransactionRecordQuery.md)

#### Account Queries

* [`AccountBalanceQuery`](reference/AccountBalanceQuery.md)

* [`AccountInfoQuery`](reference/AccountInfoQuery.md)

* [`AccountRecordsQuery`](reference/AccountRecordsQuery.md)

* [`AccountStakersQuery`](reference/AccountStakersQuery.md)

#### Contract Queries

* [`ContractBytecodeQuery`](reference/ContractBytecodeQuery.md)

* [`ContractCallQuery`](reference/ContractCallQuery.md)

* [`ContractInfoQuery`](reference/ContractInfoQuery.md)

* [`ContractRecordsQuery`](reference/ContractRecordsQuery.md)

#### File Queries

* [`FileContentsQuery`](reference/FileContentsQuery.md)

* [`FileInfoQuery`](reference/FileInfoQuery.md)

#### Topic Queries

* [`ConsensusTopicInfoQuery`](reference/ConsensusTopicInfoQuery.md)

## Contributing

We welcome participation from all developers!

To propose a change to the specifications, submit a pull request making the
change; or, open an issue for general discussion.

## License

Licensed under Apache License,
Version 2.0 – see [LICENSE](LICENSE) in this repo
or [apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)
