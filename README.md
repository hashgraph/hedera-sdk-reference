![](https://www.hedera.com/logo-capital-hbar-wordmark.jpg)

# Hedera™ Hashgraph SDK Reference

This document is the primary reference for the Hedera™ Hashgraph SDKs.

This document is normative and should be taken as the official specification for
semantic operation and classification of an **Official** Hedera™ Hashgraph SDK.

## Reference

### Core

 * [`Client`] – The protocol wrapper for the SDK, used by all transaction and query types. A `Client` is established to one network (with one or more nodes) and an optional operator account and key (to sign transactions).

### Transactions

 * [`CryptoTransferTransaction`](reference/CryptoTransferTransaction.md)

#### Accounts

 * [`AccountCreateTransaction`](reference/AccountCreateTransaction.md)

 * [`AccountUpdateTransaction`](reference/AccountUpdateTransaction.md)

 * [`AccountDeleteTransaction`](reference/AccountDeleteTransaction.md)

#### Contracts

 * [`ContractCreateTransaction`](reference/ContractCreateTransaction.md)

 * [`ContractUpdateTransaction`](reference/ContractUpdateTransaction.md)

 * [`ContractDeleteTransaction`](reference/ContractDeleteTransaction.md)

 * [`ContractExecuteTransaction`](reference/ContractExecuteTransaction.md)

#### Files

 * [`FileCreateTransaction`](reference/FileCreateTransaction.md)

 * [`FileAppendTransaction`](reference/FileAppendTransaction.md)

 * [`FileUpdateTransaction`](reference/FileUpdateTransaction.md)

 * [`FileDeleteTransaction`](reference/FileDeleteTransaction.md)

#### Consensus

 * [`ConsensusTopicCreateTransaction`](reference/ConsensusTopicCreateTransaction.md)

 * [`ConsensusTopicUpdateTransaction`](reference/ConsensusTopicUpdateTransaction.md)

 * [`ConsensusTopicDeleteTransaction`](reference/ConsensusTopicDeleteTransaction.md)

 * [`ConsensusMessageSubmitTransaction`](reference/ConsensusMessageSubmitTransaction.md)

#### System

 * [`SystemDeleteTransaction`](reference/SystemDeleteTransaction.md)

 * [`SystemUndeleteTransaction`](reference/SystemUndeleteTransaction.md)

 * [`FreezeTransaction`](reference/FreezeTransaction.md)

### Queries

#### Transactions

 * [`TransactionReceiptQuery`](reference/TransactionReceiptQuery.md)

 * [`TransactionRecordQuery`](reference/TransactionRecordQuery.md)

#### Accounts

 * [`AccountBalanceQuery`](reference/AccountBalanceQuery.md)

 * [`AccountInfoQuery`](reference/AccountInfoQuery.md)

 * [`AccountRecordsQuery`](reference/AccountRecordsQuery.md)

 * [`AccountStakersQuery`](reference/AccountStakersQuery.md)

#### Contracts

 * [`ContractBytecodeQuery`](reference/ContractBytecodeQuery.md)

 * [`ContractCallQuery`](reference/ContractCallQuery.md)

 * [`ContractInfoQuery`](reference/ContractInfoQuery.md)

 * [`ContractRecordsQuery`](reference/ContractRecordsQuery.md)

#### Files

 * [`FileContentsQuery`](reference/FileContentsQuery.md)

 * [`FileInfoQuery`](reference/FileInfoQuery.md)

#### Consensus

 * [`ConsensusTopicInfoQuery`](reference/ConsensusTopicInfoQuery.md)

## Contributing

We welcome participation from all developers! To propose a change to the specifications, submit a pull request making the change; or, open an issue for general discussion.

## License

Licensed under Apache License,
Version 2.0 – see [LICENSE](LICENSE) in this repo
or [apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)
