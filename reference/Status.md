# `enum Status`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`OK`](#ok) | ✅ | ✅ | O
| [`INVALID_TRANSACTION`](#invalid_transaction) | ✅ | ✅ | O
| [`PAYER_ACCOUNT_NOT_FOUND`](#payer_account_not_found) | ✅ | ✅ | O
| [`INVALID_NODE_ACCOUNT`](#invalid_node_account) | ✅ | ✅ | O
| [`TRANSACTION_EXPIRED`](#transaction_expired) | ✅ | ✅ | O
| [`INVALID_TRANSACTION_START`](#invalid_transaction_start) | ✅ | ✅ | O
| [`INVALID_TRANSACTION_DURATION`](#invalid_transaction_duration) | ✅ | ✅ | O
| [`INVALID_SIGNATURE`](#invalid_signature) | ✅ | ✅ | O
| [`MEMO_TOO_LONG`](#memo_too_long) | ✅ | ✅ | O
| [`INSUFFICIENT_TX_FEE`](#insufficient_tx_fee) | ✅ | ✅ | O
| [`INSUFFICIENT_PAYER_BALANCE`](#insufficient_payer_balance) | ✅ | ✅ | O
| [`DUPLICATE_TRANSACTION`](#duplicate_transaction) | ✅ | ✅ | O
| [`BUSY`](#busy) | ✅ | ✅ | O
| [`NOT_SUPPORTED`](#not_supported) | ✅ | ✅ | O
| [`INVALID_FILE_ID`](#invalid_file_id) | ✅ | ✅ | O
| [`INVALID_ACCOUNT_ID`](#invalid_account_id) | ✅ | ✅ | O
| [`INVALID_CONTRACT_ID`](#invalid_contract_id) | ✅ | ✅ | O
| [`INVALID_TRANSACTION_ID`](#invalid_transaction_id) | ✅ | ✅ | O
| [`RECEIPT_NOT_FOUND`](#receipt_not_found) | ✅ | ✅ | O
| [`RECORD_NOT_FOUND`](#record_not_found) | ✅ | ✅ | O
| [`INVALID_SOLIDITY_ID`](#invalid_solidity_id) | ✅ | ✅ | O
| [`UNKNOWN`](#unknown) | ✅ | ✅ | O
| [`SUCCESS`](#success) | ✅ | ✅ | O
| [`FAIL_INVALID`](#fail_invalid) | ✅ | ✅ | O
| [`FAIL_FEE`](#fail_fee) | ✅ | ✅ | O
| [`FAIL_BALANCE`](#fail_balance) | ✅ | ✅ | O
| [`KEY_REQUIRED`](#key_required) | ✅ | ✅ | O
| [`BAD_ENCODING`](#bad_encoding) | ✅ | ✅ | O
| [`INSUFFICIENT_ACCOUNT_BALANCE`](#insufficient_account_balance) | ✅ | ✅ | O
| [`INVALID_SOLIDITY_ADDRESS`](#invalid_solidity_address) | ✅ | ✅ | O
| [`INSUFFICIENT_GAS`](#insufficient_gas) | ✅ | ✅ | O
| [`CONTRACT_SIZE_LIMIT_EXCEEDED`](#contract_size_limit_exceeded) | ✅ | ✅ | O
| [`LOCAL_CALL_MODIFICATION_EXCEPTION`](#local_call_modification_exception) | ✅ | ✅ | O
| [`CONTRACT_REVERT_EXECUTED`](#contract_revert_executed) | ✅ | ✅ | O
| [`CONTRACT_EXECUTION_EXCEPTION`](#contract_execution_exception) | ✅ | ✅ | O
| [`INVALID_RECEIVING_NODE_ACCOUNT`](#invalid_receiving_node_account) | ✅ | ✅ | O
| [`MISSING_QUERY_HEADER`](#missing_query_header) | ✅ | ✅ | O
| [`ACCOUNT_UPDATE_FAILED`](#account_update_failed) | ✅ | ✅ | O
| [`INVALID_KEY_ENCODING`](#invalid_key_encoding) | ✅ | ✅ | O
| [`NULL_SOLIDITY_ADDRESS`](#null_solidity_address) | ✅ | ✅ | O
| [`CONTRACT_UPDATE_FAILED`](#contract_update_failed) | ✅ | ✅ | O
| [`INVALID_QUERY_HEADER`](#invalid_query_header) | ✅ | ✅ | O
| [`INVALID_FEE_SUBMITTED`](#invalid_fee_submitted) | ✅ | ✅ | O
| [`INVALID_PAYER_SIGNATURE`](#invalid_payer_signature) | ✅ | ✅ | O
| [`KEY_NOT_PROVIDED`](#key_not_provided) | ✅ | ✅ | O
| [`INVALID_EXPIRATION_TIME`](#invalid_expiration_time) | ✅ | ✅ | O
| [`NO_WACL_KEY`](#no_wacl_key) | ✅ | ✅ | O
| [`FILE_CONTENT_EMPTY`](#file_content_empty) | ✅ | ✅ | O
| [`INVALID_ACCOUNT_AMOUNTS`](#invalid_account_amounts) | ✅ | ✅ | O
| [`EMPTY_TRANSACTION_BODY`](#empty_transaction_body) | ✅ | ✅ | O
| [`INVALID_TRANSACTION_BODY`](#invalid_transaction_body) | ✅ | ✅ | O
| [`INVALID_SIGNATURE_TYPE_MISMATCHING_KEY`](#invalid_signature_type_mismatching_key) | ✅ | ✅ | O
| [`INVALID_SIGNATURE_COUNT_MISMATCHING_KEY`](#invalid_signature_count_mismatching_key) | ✅ | ✅ | O
| [`EMPTY_LIVE_HASH_BODY`](#empty_live_hash_body) | ✅ | ✅ | O
| [`EMPTY_LIVE_HASH_HASH`](#empty_live_hash_hash) | ✅ | ✅ | O
| [`EMPTY_LIVE_HASH_KEYS`](#empty_live_hash_keys) | ✅ | ✅ | O
| [`INVALID_LIVE_HASH_HASH_SIZE`](#invalid_live_hash_hash_size) | ✅ | ✅ | O
| [`EMPTY_QUERY_BODY`](#empty_query_body) | ✅ | ✅ | O
| [`EMPTY_LIVE_HASH_QUERY`](#empty_live_hash_query) | ✅ | ✅ | O
| [`LIVE_HASH_NOT_FOUND`](#live_hash_not_found) | ✅ | ✅ | O
| [`ACCOUNT_ID_DOES_NOT_EXIST`](#account_id_does_not_exist) | ✅ | ✅ | O
| [`LIVE_HASH_ALREADY_EXISTS`](#live_hash_already_exists) | ✅ | ✅ | O
| [`INVALID_FILE_WACL`](#invalid_file_wacl) | ✅ | ✅ | O
| [`SERIALIZATION_FAILED`](#serialization_failed) | ✅ | ✅ | O
| [`TRANSACTION_OVERSIZE`](#transaction_oversize) | ✅ | ✅ | O
| [`TRANSACTION_TOO_MANY_LAYERS`](#transaction_too_many_layers) | ✅ | ✅ | O
| [`CONTRACT_DELETED`](#contract_deleted) | ✅ | ✅ | O
| [`PLATFORM_NOT_ACTIVE`](#platform_not_active) | ✅ | ✅ | O
| [`KEY_PREFIX_MISMATCH`](#key_prefix_mismatch) | ✅ | ✅ | O
| [`PLATFORM_TRANSACTION_NOT_CREATED`](#platform_transaction_not_created) | ✅ | ✅ | O
| [`INVALID_RENEWAL_PERIOD`](#invalid_renewal_period) | ✅ | ✅ | O
| [`INVALID_PAYER_ACCOUNT_ID`](#invalid_payer_account_id) | ✅ | ✅ | O
| [`ACCOUNT_DELETED`](#account_deleted) | ✅ | ✅ | O
| [`FILE_DELETED`](#file_deleted) | ✅ | ✅ | O
| [`ACCOUNT_REPEATED_IN_ACCOUNT_AMOUNTS`](#account_repeated_in_account_amounts) | ✅ | ✅ | O
| [`SETTING_NEGATIVE_ACCOUNT_BALANCE`](#setting_negative_account_balance) | ✅ | ✅ | O
| [`OBTAINER_REQUIRED`](#obtainer_required) | ✅ | ✅ | O
| [`OBTAINER_SAME_CONTRACT_ID`](#obtainer_same_contract_id) | ✅ | ✅ | O
| [`OBTAINER_DOES_NOT_EXIST`](#obtainer_does_not_exist) | ✅ | ✅ | O
| [`MODIFYING_IMMUTABLE_CONTRACT`](#modifying_immutable_contract) | ✅ | ✅ | O
| [`FILE_SYSTEM_EXCEPTION`](#file_system_exception) | ✅ | ✅ | O
| [`AUTORENEW_DURATION_NOT_IN_RANGE`](#autorenew_duration_not_in_range) | ✅ | ✅ | O
| [`ERROR_DECODING_BYTESTRING`](#error_decoding_bytestring) | ✅ | ✅ | O
| [`CONTRACT_FILE_EMPTY`](#contract_file_empty) | ✅ | ✅ | O
| [`CONTRACT_BYTECODE_EMPTY`](#contract_bytecode_empty) | ✅ | ✅ | O
| [`INVALID_INITIAL_BALANCE`](#invalid_initial_balance) | ✅ | ✅ | O
| [`INVALID_RECEIVE_RECORD_THRESHOLD`](#invalid_receive_record_threshold) | ✅ | ✅ | O
| [`INVALID_SEND_RECORD_THRESHOLD`](#invalid_send_record_threshold) | ✅ | ✅ | O
| [`ACCOUNT_IS_NOT_GENESIS_ACCOUNT`](#account_is_not_genesis_account) | ✅ | ✅ | O
| [`PAYER_ACCOUNT_UNAUTHORIZED`](#payer_account_unauthorized) | ✅ | ✅ | O
| [`INVALID_FREEZE_TRANSACTION_BODY`](#invalid_freeze_transaction_body) | ✅ | ✅ | O
| [`FREEZE_TRANSACTION_BODY_NOT_FOUND`](#freeze_transaction_body_not_found) | ✅ | ✅ | O
| [`TRANSFER_LIST_SIZE_LIMIT_EXCEEDED`](#transfer_list_size_limit_exceeded) | ✅ | ✅ | O
| [`RESULT_SIZE_LIMIT_EXCEEDED`](#result_size_limit_exceeded) | ✅ | ✅ | O
| [`NOT_SPECIAL_ACCOUNT`](#not_special_account) | ✅ | ✅ | O
| [`CONTRACT_NEGATIVE_GAS`](#contract_negative_gas) | ✅ | ✅ | O
| [`CONTRACT_NEGATIVE_VALUE`](#contract_negative_value) | ✅ | ✅ | O
| [`INVALID_FEE_FILE`](#invalid_fee_file) | ✅ | ✅ | O
| [`INVALID_EXCHANGE_RATE_FILE`](#invalid_exchange_rate_file) | ✅ | ✅ | O
| [`INSUFFICIENT_LOCAL_CALL_GAS`](#insufficient_local_call_gas) | ✅ | ✅ | O
| [`ENTITY_NOT_ALLOWED_TO_DELETE`](#entity_not_allowed_to_delete) | ✅ | ✅ | O
| [`AUTHORIZATION_FAILED`](#authorization_failed) | ✅ | ✅ | O
| [`FILE_UPLOADED_PROTO_INVALID`](#file_uploaded_proto_invalid) | ✅ | ✅ | O
| [`FILE_UPLOADED_PROTO_NOT_SAVED_TO_DISK`](#file_uploaded_proto_not_saved_to_disk) | ✅ | ✅ | O
| [`FEE_SCHEDULE_FILE_PART_UPLOADED`](#fee_schedule_file_part_uploaded) | ✅ | ✅ | O
| [`EXCHANGE_RATE_CHANGE_LIMIT_EXCEEDED`](#exchange_rate_change_limit_exceeded) | ✅ | ✅ | O
| [`MAX_CONTRACT_STORAGE_EXCEEDED`](#max_contract_storage_exceeded) | ✅ | ✅ | O
| [`TRANSFER_ACCOUNT_SAME_AS_DELETE_ACCOUNT`](#transfer_account_same_as_delete_account) | ✅ | ✅ | O
| [`TOTAL_LEDGER_BALANCE_INVALID`](#total_ledger_balance_invalid) | ✅ | ✅ | O
| [`EXPIRATION_REDUCTION_NOT_ALLOWED`](#expiration_reduction_not_allowed) | ✅ | ✅ | O
| [`MAX_GAS_LIMIT_EXCEEDED`](#max_gas_limit_exceeded) | ✅ | ✅ | O
| [`MAX_FILE_SIZE_EXCEEDED`](#max_file_size_exceeded) | ✅ | ✅ | O
| [`INVALID_TOPIC_ID`](#invalid_topic_id) | ✅ | ✅ | O
| [`INVALID_ADMIN_KEY`](#invalid_admin_key) | ✅ | ✅ | O
| [`INVALID_SUBMIT_KEY`](#invalid_submit_key) | ✅ | ✅ | O
| [`UNAUTHORIZED`](#unauthorized) | ✅ | ✅ | O
| [`INVALID_TOPIC_MESSAGE`](#invalid_topic_message) | ✅ | ✅ | O
| [`INVALID_AUTORENEW_ACCOUNT`](#invalid_autorenew_account) | ✅ | ✅ | O
| [`AUTORENEW_ACCOUNT_NOT_ALLOWED`](#autorenew_account_not_allowed) | ✅ | ✅ | O
| [`TOPIC_EXPIRED`](#topic_expired) | ✅ | ✅ | O
| [`INVALID_CHUNK_NUMBER`](#invalid_chunk_number) | ✅ | ✅ | O
| [`INVALID_CHUNK_TRANSACTION_ID`](#invalid_chunk_transaction_id) | ✅ | ✅ | O

## Variants

### `OK`

The transaction passed the pre-check validation.

### `INVALID_TRANSACTION`

For any error not handled by specific error codes listed below.

### `PAYER_ACCOUNT_NOT_FOUND`

Payer account does not exist.

### `INVALID_NODE_ACCOUNT`

Node Account provided does not match the node account of the node the transaction was
submitted to.

### `TRANSACTION_EXPIRED`

Pre-Check error when TransactionValidStart + transactionValidDuration is less than current
consensus time.

### `INVALID_TRANSACTION_START`

Transaction start time is greater than current consensus time

### `INVALID_TRANSACTION_DURATION`

valid transaction duration is a positive non zero number that does not exceed 120 seconds

### `INVALID_SIGNATURE`

The transaction signature is not valid

### `MEMO_TOO_LONG`

Transaction memo size exceeded 100 bytes

### `INSUFFICIENT_TX_FEE`

The fee provided in the transaction is insufficient for this type of transaction

### `INSUFFICIENT_PAYER_BALANCE`

The payer account has insufficient cryptocurrency to pay the transaction fee

### `DUPLICATE_TRANSACTION`

This transaction ID is a duplicate of one that was submitted to this node or reached
consensus in the last 180 seconds (receipt period)

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

contract byte code size is over the limit

### `LOCAL_CALL_MODIFICATION_EXCEPTION`

local execution (query) is requested for a function which changes state

### `CONTRACT_REVERT_EXECUTED`

Contract REVERT OPCODE executed

### `CONTRACT_EXECUTION_EXCEPTION`

For any contract execution related error not handled by specific error codes listed above.

### `INVALID_RECEIVING_NODE_ACCOUNT`

In Query validation, account with +ve(amount) value should be Receiving node account, the
receiver account should be only one account in the list

### `MISSING_QUERY_HEADER`

Header is missing in Query request

### `ACCOUNT_UPDATE_FAILED`

The update of the account failed

### `INVALID_KEY_ENCODING`

Provided key encoding was not supported by the system

### `NULL_SOLIDITY_ADDRESS`

null solidity address

### `CONTRACT_UPDATE_FAILED`

update of the contract failed

### `INVALID_QUERY_HEADER`

the query header is invalid

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

the type of key (base ed25519 key, KeyList, or ThresholdKey) does not match the type of
signature (base ed25519 signature, SignatureList, or ThresholdKeySignature)

### `INVALID_SIGNATURE_COUNT_MISMATCHING_KEY`

the number of key (KeyList, or ThresholdKey) does not match that of signature (SignatureList,
or ThresholdKeySignature). e.g. if a keyList has 3 base keys, then the corresponding
signatureList should also have 3 base signatures.

### `EMPTY_LIVE_HASH_BODY`

the claim body is empty

### `EMPTY_LIVE_HASH_HASH`

the hash for the claim is empty

### `EMPTY_LIVE_HASH_KEYS`

the key list is empty

### `INVALID_LIVE_HASH_HASH_SIZE`

the size of the claim hash is not 48 bytes

### `EMPTY_QUERY_BODY`

the query body is empty

### `EMPTY_LIVE_HASH_QUERY`

the crypto claim query is empty

### `LIVE_HASH_NOT_FOUND`

the crypto claim doesn't exists in the file system. It expired or was never persisted.

### `ACCOUNT_ID_DOES_NOT_EXIST`

the account id passed has not yet been created.

### `LIVE_HASH_ALREADY_EXISTS`

the claim hash already exists

### `INVALID_FILE_WACL`

File WACL keys are invalid

### `SERIALIZATION_FAILED`

Serialization failure

### `TRANSACTION_OVERSIZE`

The size of the Transaction is greater than transactionMaxBytes

### `TRANSACTION_TOO_MANY_LAYERS`

The Transaction has more than 50 levels

### `CONTRACT_DELETED`

Contract is marked as deleted

### `PLATFORM_NOT_ACTIVE`

the platform node is either disconnected or lagging behind.

### `KEY_PREFIX_MISMATCH`

one public key matches more than one prefixes on the signature map

### `PLATFORM_TRANSACTION_NOT_CREATED`

transaction not created by platform due to either large backlog or message size exceeded
transactionMaxBytes

### `INVALID_RENEWAL_PERIOD`

auto renewal period is not a positive number of seconds

### `INVALID_PAYER_ACCOUNT_ID`

the response code when a smart contract id is passed for a crypto API request

### `ACCOUNT_DELETED`

the account has been marked as deleted

### `FILE_DELETED`

the file has been marked as deleted

### `ACCOUNT_REPEATED_IN_ACCOUNT_AMOUNTS`

same accounts repeated in the transfer account list

### `SETTING_NEGATIVE_ACCOUNT_BALANCE`

attempting to set negative balance value for crypto account

### `OBTAINER_REQUIRED`

when deleting smart contract that has crypto balance either transfer account or transfer
smart contract is required

### `OBTAINER_SAME_CONTRACT_ID`

when deleting smart contract that has crypto balance you can not use the same contract id as
transferContractId as the one being deleted

### `OBTAINER_DOES_NOT_EXIST`

transferAccountId or transferContractId specified for contract delete does not exist

### `MODIFYING_IMMUTABLE_CONTRACT`

attempting to modify (update or delete a immutable smart contract, i.e. one created without a
admin key)

### `FILE_SYSTEM_EXCEPTION`

Unexpected exception thrown by file system functions

### `AUTORENEW_DURATION_NOT_IN_RANGE`

the duration is not a subset of [MINIMUM_AUTORENEW_DURATION,MAXIMUM_AUTORENEW_DURATION]

### `ERROR_DECODING_BYTESTRING`

Decoding the smart contract binary to a byte array failed. Check that the input is a valid
hex string.

### `CONTRACT_FILE_EMPTY`

File to create a smart contract was of length zero

### `CONTRACT_BYTECODE_EMPTY`

Bytecode for smart contract is of length zero

### `INVALID_INITIAL_BALANCE`

Attempt to set negative initial balance

### `INVALID_RECEIVE_RECORD_THRESHOLD`

attempt to set negative receive record threshold

### `INVALID_SEND_RECORD_THRESHOLD`

attempt to set negative send record threshold

### `ACCOUNT_IS_NOT_GENESIS_ACCOUNT`

Special Account Operations should be performed by only Genesis account, return this code if
it is not Genesis Account

### `PAYER_ACCOUNT_UNAUTHORIZED`

The fee payer account doesn't have permission to submit such Transaction

### `INVALID_FREEZE_TRANSACTION_BODY`

FreezeTransactionBody is invalid

### `FREEZE_TRANSACTION_BODY_NOT_FOUND`

FreezeTransactionBody does not exist

### `TRANSFER_LIST_SIZE_LIMIT_EXCEEDED`

Exceeded the number of accounts (both from and to) allowed for crypto transfer list

### `RESULT_SIZE_LIMIT_EXCEEDED`

Smart contract result size greater than specified maxResultSize

### `NOT_SPECIAL_ACCOUNT`

The payer account is not a special account(account 0.0.55)

### `CONTRACT_NEGATIVE_GAS`

Negative gas was offered in smart contract call

### `CONTRACT_NEGATIVE_VALUE`

Negative value / initial balance was specified in a smart contract call / create

### `INVALID_FEE_FILE`

Failed to update fee file

### `INVALID_EXCHANGE_RATE_FILE`

Failed to update exchange rate file

### `INSUFFICIENT_LOCAL_CALL_GAS`

Payment tendered for contract local call cannot cover both the fee and the gas

### `ENTITY_NOT_ALLOWED_TO_DELETE`

Entities with Entity ID below 1000 are not allowed to be deleted

### `AUTHORIZATION_FAILED`

Violating one of these rules: 1) treasury account can update all entities below 0.0.1000, 2)
account 0.0.50 can update all entities from 0.0.51 - 0.0.80, 3) Network Function Master
Account A/c 0.0.50 - Update all Network Function accounts &amp; perform all the Network Functions
listed below, 4) Network Function Accounts: i) A/c 0.0.55 - Update Address Book files
 iii) A/c 0.0.57 - Update
Exchange Rate (0.0.112).

### `FILE_UPLOADED_PROTO_INVALID`

Fee Schedule Proto uploaded but not valid (append or update is required)

### `FILE_UPLOADED_PROTO_NOT_SAVED_TO_DISK`

Fee Schedule Proto uploaded but not valid (append or update is required)

### `FEE_SCHEDULE_FILE_PART_UPLOADED`

Fee Schedule Proto File Part uploaded

### `EXCHANGE_RATE_CHANGE_LIMIT_EXCEEDED`

The change on Exchange Rate exceeds Exchange_Rate_Allowed_Percentage

### `MAX_CONTRACT_STORAGE_EXCEEDED`

Contract permanent storage exceeded the currently allowable limit

### `TRANSFER_ACCOUNT_SAME_AS_DELETE_ACCOUNT`

Transfer Account should not be same as Account to be deleted

### `TOTAL_LEDGER_BALANCE_INVALID`

The ledger balance is invalid

### `EXPIRATION_REDUCTION_NOT_ALLOWED`

The expiration date/time on a smart contract may not be reduced

### `MAX_GAS_LIMIT_EXCEEDED`

Gas exceeded currently allowable gas limit per transaction

### `MAX_FILE_SIZE_EXCEEDED`

File size exceeded the currently allowable limit

### `INVALID_TOPIC_ID`

The Topic ID specified is not in the system.

### `INVALID_ADMIN_KEY`

The admin key provided is invalid

### `INVALID_SUBMIT_KEY`

The submit key provided is invalid

### `UNAUTHORIZED`

An attempted operation was not authorized (ie - a deleteTopic for a topic with no adminKey).

### `INVALID_TOPIC_MESSAGE`

A ConsensusService message is empty.

### `INVALID_AUTORENEW_ACCOUNT`

The autoRenewAccount specified is not a valid, active account.

### `AUTORENEW_ACCOUNT_NOT_ALLOWED`

An adminKey was not specified on the topic, so there must not be an autoRenewAccount.

### `TOPIC_EXPIRED`

The topic has expired, was not automatically renewed, and is in a 7 day grace period before
the topic will be deleted unrecoverably. This error response code will not be returned until
autoRenew functionality is supported by HAPI.

### `INVALID_CHUNK_NUMBER`

chunk number must be from 1 to total (chunks) inclusive.

### `INVALID_CHUNK_TRANSACTION_ID`

For every chunk, the payer account that is part of initialTransactionID must match the Payer Account of this transaction. The entire initialTransactionID should match the transactionID of the first chunk, but this is not checked or enforced by Hedera except when the chunk number is 1.
