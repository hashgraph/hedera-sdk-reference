# Hedera™ Hashgraph SDK

![Hedera Hasgraph](https://www.hedera.com/logo-capital-hbar-wordmark.jpg)

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

* [`TransactionId`](reference/TransactionId.md)
* [`TransactionReceipt`](reference/TransactionReceipt.md)
* [`TransactionRecord`](reference/TransactionRecord.md)
* [`TransactionResponse`](reference/TransactionResponse.md)

---

* [`Query`](reference/core/Query.md)
* [`TransactionReceiptQuery`](reference/TransactionReceiptQuery.md)
* [`TransactionRecordQuery`](reference/TransactionRecordQuery.md)

### Errors

* [`PrecheckStatus`](reference/error/PrecheckStatus.md)
* [`ReceiptStatus`](reference/error/ReceiptStatus.md)
* [`MaxQueryPaymentExceeded`](reference/cryptography/MaxQueryPaymentExceeded.md)
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

* [`AccountId`](reference/AccountId.md)
* [`AccountInfo`](reference/AccountInfo.md)

---

* [`CryptoTransferTransaction`](reference/CryptoTransferTransaction.md)
* [`AccountCreateTransaction`](reference/AccountCreateTransaction.md)
* [`AccountUpdateTransaction`](reference/AccountUpdateTransaction.md)
* [`AccountDeleteTransaction`](reference/AccountDeleteTransaction.md)

---

* [`AccountBalanceQuery`](reference/AccountBalanceQuery.md)
* [`AccountInfoQuery`](reference/AccountInfoQuery.md)
* [`AccountRecordsQuery`](reference/AccountRecordsQuery.md)
* [`AccountStakersQuery`](reference/AccountStakersQuery.md)

### Smart Contract

* [`ContractId`](reference/ContractId.md)
* [`ContractInfo`](reference/ContractInfo.md)

---

* [`ContractCreateTransaction`](reference/ContractCreateTransaction.md)
* [`ContractUpdateTransaction`](reference/ContractUpdateTransaction.md)
* [`ContractDeleteTransaction`](reference/ContractDeleteTransaction.md)
* [`ContractExecuteTransaction`](reference/ContractExecuteTransaction.md)

---

* [`ContractBytecodeQuery`](reference/ContractBytecodeQuery.md)
* [`ContractCallQuery`](reference/ContractCallQuery.md)
* [`ContractInfoQuery`](reference/ContractInfoQuery.md)
* [`ContractRecordsQuery`](reference/ContractRecordsQuery.md)

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

## License

Licensed under Apache License,
Version 2.0 – see [LICENSE](LICENSE) in this repo
or [apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)
