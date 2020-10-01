# `enum Status`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`TINYBAR`](#tinybar) | ✅ | ✅ | O
| [`MICROBAR`](#microbar) | ✅ | ✅ | O
## Variants
     
### `OK`

The transaction passed the pre-check validation.

### `INVALID_TRANSACTION`

For any error not handled by specific error codes listed below.

### `PAYER_ACCOUNT_NOT_FOUND`

Payer account does not exist.

### `INVALID_NODE_ACCOUNT`

Node Account provided does not match the node account of the node the transaction was submitted to.

### `TRANSACTION_EXPIRED`

Pre-Check error when TransactionValidStart + transactionValidDuration is less than current consensus time.

### ` INVALID_TRANSACTION_START`

Transaction start time is greater than current consensus time

### `INVALID_TRANSACTION_DURATION`

Valid transaction duration is a positive non zero number that does not exceed 120 seconds

### `INVALID_SIGNATURE`

The transaction signature is not valid

### `MEMO_TOO_LONG`

Transaction memo size exceeded 100 bytes

### `INSUFFICIENT_TX_FEE`

The fee provided in the transaction is insufficient for this type of transaction.

### `INSUFFICIENT_PAYER_BALANCE`

The payer account has insufficient cryptocurrency to pay the transaction fee.

### `DUPLICATE_TRANSACTION`

This transaction ID is a duplicate of one that was submitted to this node or reached consensus in the last 180 seconds (receipt period).

### `BUSY`

If API is throttled out

### `NOT_SUPPORTED`

The API is not currently supported

### `INVALID_FILE_ID`

The file id is invalid or does not exist

### `INVALID_ACCOUNT_ID`

The account id is invalid or does not exist

### `INVALID_CONTRACT_ID`

The contract id is invalid or does not exist

### `INVALID_TRANSACTION_ID`

Transaction id is not valid

### `RECEIPT_NOT_FOUND`

Receipt for given transaction id does not exist

### `RECORD_NOT_FOUND`

Record for given transaction id does not exist

### `INVALID_SOLIDITY_ID`

The solidity id is invalid or entity with this solidity id does not exist

### `UNKNOWN`

Transaction hasn't yet reached consensus, or has already expired

### `SUCCESS`

The transaction succeeded

### `FAIL_INVALID`

There was a system error and the transaction failed because of invalid request parameters.

### `FAIL_FEE`

There was a system error while performing fee calculation, reserved for future.

### `FAIL_BALANCE`

There was a system error while performing balance checks, reserved for future.

### `KEY_REQUIRED`

Key not provided in the transaction body

### `BAD_ENCODING`

Unsupported algorithm/encoding used for keys in the transaction

### `INSUFFICIENT_ACCOUNT_BALANCE`

When the account balance is not sufficient for the transfer

### `INVALID_SOLIDITY_ADDRESS`

During an update transaction when the system is not able to find the Users Solidity address

### `INSUFFICIENT_GAS`

Not enough gas was supplied to execute transaction

### `CONTRACT_SIZE_LIMIT_EXCEEDED`

Contract byte code size is over the limit

### `LOCAL_CALL_MODIFICATION_EXCEPTION`

Local execution (query) is requested for a function which changes state

### `CONTRACT_REVERT_EXECUTED`

Contract REVERT OPCODE executed

### `CONTRACT_EXECUTION_EXCEPTION`

For any contract execution related error not handled by specific error codes listed above.

### `INVALID_RECEIVING_NODE_ACCOUNT`

In Query validation, account with +ve(amount) value should be Receiving node account, the receiver account should be only one account in the list

### `MISSING_QUERY_HEADER`

Header is missing in Query request

### `ACCOUNT_UPDATE_FAILED`

The update of the account failed

### `INVALID_KEY_ENCODING`

Provided key encoding was not supported by the system

### `NULL_SOLIDITY_ADDRESS`

null solidity address

### `CONTRACT_UPDATE_FAILED`

Update of the contract failed

### `INVALID_QUERY_HEADER`

The query header is invalid

### `INVALID_FEE_SUBMITTED`

Invalid fee submitted

### `INVALID_PAYER_SIGNATURE`

Payer signature is invalid

### `KEY_NOT_PROVIDED`

The keys were not provided in the request.

### `INVALID_EXPIRATION_TIME`

Expiration time provided in the transaction was invalid.

### `NO_WACL_KEY`

WriteAccess Control Keys are not provided for the file

### `FILE_CONTENT_EMPTY`

The contents of file are provided as empty.

### `INVALID_ACCOUNT_AMOUNTS`

The crypto transfer credit and debit do not sum equal to 0

### `EMPTY_TRANSACTION_BODY`

Transaction body provided is empty

### `INVALID_TRANSACTION_BODY`

Invalid transaction body provided

### `INVALID_SIGNATURE_TYPE_MISMATCHING_KEY`

The type of key (base ed25519 key, KeyList, or ThresholdKey) does not match the type of
signature (base ed25519 signature, SignatureList, or ThresholdKeySignature)

### `INVALID_SIGNATURE_COUNT_MISMATCHING_KEY`

The number of key (KeyList, or ThresholdKey) does not match that of signature (SignatureList,
or ThresholdKeySignature). e.g. if a keyList has 3 base keys, then the corresponding
signatureList should also have 3 base signatures.

### `EMPTY_LIVE_HASH_BODY`

The claim body is empty

### `EMPTY_LIVE_HASH_HASH`

the key list is empty

### `INVALID_LIVE_HASH_HASH_SIZE`

the size of the claim hash is not 48 bytes

### `OK`

### `OK`

### `OK`

### `OK`

### `OK`

### `OK`

### `OK`





