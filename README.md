# Hedera™ Hashgraph SDK

![Hedera Hashgraph](https://www.hedera.com/logo-capital-hbar-wordmark.jpg)

This document is the primary reference for the Hedera™ Hashgraph SDKs.

This document is normative and should be taken as the official specification for
semantic operation and classification of an **Official** Hedera™ Hashgraph SDK.

## Reference

### Core

* [`Client`](reference/core/Client.md)
* [`Status`](reference/Status.md)

---

* [`Transaction`](reference/core/Transaction.md)

---

* [`TransactionId`](reference/core/TransactionId.md)
* [`TransactionReceipt`](reference/core/TransactionReceipt.md)
* [`TransactionRecord`](reference/core/TransactionRecord.md)
* [`TransactionResponse`](reference/core/TransactionResponse.md)

---

* [`Query`](reference/core/Query.md)
* [`TransactionReceiptQuery`](reference/core/TransactionReceiptQuery.md)
* [`TransactionRecordQuery`](reference/core/TransactionRecordQuery.md)

### Errors

* [`PrecheckStatus`](reference/error/PrecheckStatus.md)
* [`ReceiptStatus`](reference/error/ReceiptStatus.md)
* [`MaxQueryPaymentExceeded`](reference/error/MaxQueryPaymentExceeded.md)
* [`BadKey`](reference/error/BadKey.md)
* [`BadMnemonic`](reference/error/BadMnemonic.md)
* [`BadMnemonicReason`](reference/error/BadMnemonicReason.md)

### Cryptography

* [`Key`](reference/cryptography/Key.md)
* [`KeyList`](reference/cryptography/KeyList.md)
* [`PrivateKey`](reference/cryptography/PrivateKey.md)
* [`PublicKey`](reference/cryptography/PublicKey.md)
* [`Mnemonic`](reference/cryptography/Mnemonic.md)

### Cryptocurrency

* [`AccountId`](reference/cryptocurrency/AccountId.md)
* [`AccountInfo`](reference/cryptocurrency/AccountInfo.md)

---

* [`CryptoTransferTransaction`](reference/cryptocurrency/CryptoTransferTransaction.md)
* [`AccountCreateTransaction`](reference/cryptocurrency/AccountCreateTransaction.md)
* [`AccountUpdateTransaction`](reference/cryptocurrency/AccountUpdateTransaction.md)
* [`AccountDeleteTransaction`](reference/cryptocurrency/AccountDeleteTransaction.md)

---

* [`AccountBalanceQuery`](reference/cryptocurrency/AccountBalanceQuery.md)
* [`AccountInfoQuery`](reference/cryptocurrency/AccountInfoQuery.md)
* [`AccountRecordsQuery`](reference/cryptocurrency/AccountRecordsQuery.md)
* [`AccountStakersQuery`](reference/cryptocurrency/AccountStakersQuery.md)

### Smart Contract

* [`ContractId`](reference/contract/ContractId.md)
* [`ContractInfo`](reference/contract/ContractInfo.md)

---

* [`ContractCreateTransaction`](reference/contract/ContractCreateTransaction.md)
* [`ContractUpdateTransaction`](reference/contract/ContractUpdateTransaction.md)
* [`ContractDeleteTransaction`](reference/contract/ContractDeleteTransaction.md)
* [`ContractExecuteTransaction`](reference/contract/ContractExecuteTransaction.md)
* [`ContractCreateFlow`](reference/contract/ContractCreateFlow.md)

---

* [`ContractBytecodeQuery`](reference/contract/ContractBytecodeQuery.md)
* [`ContractCallQuery`](reference/contract/ContractCallQuery.md)
* [`ContractInfoQuery`](reference/contract/ContractInfoQuery.md)
* [`ContractRecordsQuery`](reference/contract/ContractRecordsQuery.md)

### File

* [`FileId`](reference/FileId.md)
* [`FileInfo`](reference/FileInfo.md)

---

* [`FileCreateTransaction`](reference/FileCreateTransaction.md)
* [`FileAppendTransaction`](reference/FileAppendTransaction.md)
* [`FileUpdateTransaction`](reference/FileUpdateTransaction.md)
* [`FileDeleteTransaction`](reference/FileDeleteTransaction.md)

---

* [`FileContentsQuery`](reference/FileContentsQuery.md)
* [`FileInfoQuery`](reference/FileInfoQuery.md)

### Consensus Topic

* [`TopicId`](reference/TopicId.md)
* [`TopicInfo`](reference/TopicInfo.md)

---

* [`TopicCreateTransaction`](reference/TopicCreateTransaction.md)
* [`TopicUpdateTransaction`](reference/TopicUpdateTransaction.md)
* [`TopicDeleteTransaction`](reference/TopicDeleteTransaction.md)
* [`TopicMessageSubmitTransaction`](reference/TopicMessageSubmitTransaction.md)

---

* [`ConsensusTopicInfoQuery`](reference/ConsensusTopicInfoQuery.md)

### System

* [`SystemDeleteTransaction`](reference/SystemDeleteTransaction.md)
* [`SystemUndeleteTransaction`](reference/SystemUndeleteTransaction.md)
* [`FreezeTransaction`](reference/FreezeTransaction.md)

### Network

* [`NetworkVersionQuery`](reference/NetworkVersionQuery.md)

## Contributing

We welcome participation from all developers!

To propose a change to the specifications, submit a pull request making the
change; or, open an issue for general discussion.

Please check out
[contributing guide](https://github.com/hashgraph/.github/blob/main/CONTRIBUTING.md)
to see how you can get involved.

## Code of Conduct

This project is governed by the
[Contributor Covenant Code of Conduct](https://github.com/hashgraph/.github/blob/main/CODE_OF_CONDUCT.md). By
participating, you are expected to uphold this code of conduct. Please report unacceptable behavior
to [oss@hedera.com](mailto:oss@hedera.com).

## License

[Apache License 2.0](LICENSE)
