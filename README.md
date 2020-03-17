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

 * [`AccountCreateTransaction`]

 * [`AccountUpdateTransaction`]

 * [`AccountDeleteTransaction`](reference/AccountDeleteTransaction.md)

#### Contracts

 * [`ContractCreateTransaction`]

 * [`ContractUpdateTransaction`]

 * [`ContractDeleteTransaction`]

 * [`ContractExecuteTransaction`]

#### Files

 * [`FileCreateTransaction`]

 * [`FileAppendTransaction`]

 * [`FileUpdateTransaction`]

 * [`FileDeleteTransaction`]

#### Consensus

 * [`ConsensusTopicCreateTransaction`]

 * [`ConsensusTopicUpdateTransaction`]

 * [`ConsensusTopicDeleteTransaction`]

 * [`ConsensusMessageSubmitTransaction`]

#### System

 * [`SystemDeleteTransaction`]

 * [`SystemUndeleteTransaction`]

 * [`FreezeTransaction`]

### Queries

#### Transactions

 * [`TransactionReceiptQuery`]

 * [`TransactionRecordQuery`]

#### Accounts

 * [`AccountBalanceQuery`]

 * [`AccountInfoQuery`]

 * [`AccountRecordsQuery`]

 * [`AccountStakersQuery`]

#### Contracts

 * [`ContractBytecodeQuery`]

 * [`ContractCallQuery`]

 * [`ContractInfoQuery`]

 * [`ContractRecordsQuery`]

#### Files

 * [`FileContentsQuery`]

 * [`FileInfoQuery`]

#### Consensus

 * [`ConsensusTopicInfoQuery`]

## Contributing

We welcome participation from all developers! To propose a change to the specifications, submit a pull request making the change; or, open an issue for general discussion.

## License

Licensed under Apache License,
Version 2.0 – see [LICENSE](LICENSE) in this repo
or [apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)
