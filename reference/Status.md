# `Status`

> enum `Status`

### Variants

##### OK

The transaction passed the precheck validations.

##### INVALID_TRANSACTION

For any error not handled by specific error codes listed below.

##### PAYER_ACCOUNT_NOT_FOUND

Payer account does not exist.

##### INVALID_NODE_ACCOUNT

Node Account provided does not match the node account of the node the transaction was submitted to.

##### TRANSACTION_EXPIRED

Pre-Check error when TransactionValidStart + transactionValidDuration is less than current consensus time.

##### INVALID_TRANSACTION_START

Transaction start time is greater than current consensus time

##### INVALID_TRANSACTION_DURATION

Valid transaction duration is a positive non zero number that does not exceed 120 seconds

##### INVALID_SIGNATURE

The transaction signature is not valid

##### MEMO_TOO_LONG

Transaction memo size exceeded 100 bytes

##### INSUFFICIENT_TX_FEE

The fee provided in the transaction is insufficient for this type of transaction

##### INSUFFICIENT_PAYER_BALANCE

The payer account has insufficient cryptocurrency to pay the transaction fee

##### DUPLICATE_TRANSACTION

This transaction ID is a duplicate of one that was submitted to this node or reached consensus in the last 180 seconds (receipt period)

##### BUSY

If API is throttled out

##### NOT_SUPPORTED

The API is not currently supported

##### INVALID_FILE_ID

The file id is invalid or does not exist

##### INVALID_ACCOUNT_ID

The account id is invalid or does not exist

##### INVALID_CONTRACT_ID

The contract id is invalid or does not exist

##### INVALID_TRANSACTION_ID

Transaction id is not valid

##### RECEIPT_NOT_FOUND

Receipt for given transaction id does not exist

##### RECORD_NOT_FOUND

Record for given transaction id does not exist

##### INVALID_SOLIDITY_ID

The solidity id is invalid or entity with this solidity id does not exist

##### UNKNOWN

The responding node has submitted the transaction to the network. Its final status is still unknown.

##### SUCCESS

The transaction succeeded

##### FAIL_INVALID

There was a system error and the transaction failed because of invalid request parameters.

##### FAIL_FEE

There was a system error while performing fee calculation, reserved for future.

##### FAIL_BALANCE

There was a system error while performing balance checks, reserved for future.

##### KEY_REQUIRED

Key not provided in the transaction body

##### BAD_ENCODING

Unsupported algorithm/encoding used for keys in the transaction

##### INSUFFICIENT_ACCOUNT_BALANCE

When the account balance is not sufficient for the transfer

##### INVALID_SOLIDITY_ADDRESS

During an update transaction when the system is not able to find the Users Solidity address

##### INSUFFICIENT_GAS

Not enough gas was supplied to execute transaction

##### CONTRACT_SIZE_LIMIT_EXCEEDED

Contract byte code size is over the limit

##### LOCAL_CALL_MODIFICATION_EXCEPTION

Local execution (query) is requested for a function which changes state

##### CONTRACT_REVERT_EXECUTED

Contract REVERT OPCODE executed

##### CONTRACT_EXECUTION_EXCEPTION

For any contract execution related error not handled by specific error codes listed above.

##### INVALID_RECEIVING_NODE_ACCOUNT

In Query validation, account with +ve(amount) value should be Receiving node account, the receiver account should be only one account in the list

##### MISSING_QUERY_HEADER

Header is missing in Query request

##### ACCOUNT_UPDATE_FAILED

The update of the account failed

##### INVALID_KEY_ENCODING

Provided key encoding was not supported by the system

##### NULL_SOLIDITY_ADDRESS

Null solidity address

##### CONTRACT_UPDATE_FAILED

Update of the contract failed

##### INVALID_QUERY_HEADER

The query header is invalid

##### INVALID_FEE_SUBMITTED

Invalid fee submitted

##### INVALID_PAYER_SIGNATURE

Payer signature is invalid

##### KEY_NOT_PROVIDED

The keys were not provided in the request.

##### INVALID_EXPIRATION_TIME

Expiration time provided in the transaction was invalid.

##### NO_WACL_KEY

WriteAccess Control Keys are not provided for the file

##### FILE_CONTENT_EMPTY

The contents of file are provided as empty.

##### INVALID_ACCOUNT_AMOUNTS

The crypto transfer credit and debit do not sum equal to 0

##### EMPTY_TRANSACTION_BODY

Transaction body provided is empty

##### INVALID_TRANSACTION_BODY

Invalid transaction body provided

##### INVALID_SIGNATURE_TYPE_MISMATCHING_KEY

The type of key (base ed25519 key, KeyList, or ThresholdKey) does not match the type of signature (base ed25519 signature, SignatureList, or ThresholdKeySignature)

##### INVALID_SIGNATURE_COUNT_MISMATCHING_KEY

The number of key (KeyList, or ThresholdKey) does not match that of signature (SignatureList, or ThresholdKeySignature). e.g. if a keyList has 3 base keys, then the corresponding signatureList should also have 3 base signatures.

##### EMPTY_LIVE_HASH_BODY

The livehash body is empty

##### EMPTY_LIVE_HASH

The livehash data is missing

##### EMPTY_LIVE_HASH_KEYS

The keys for a livehash are missing

##### INVALID_LIVE_HASH_SIZE

The livehash data is not the output of a SHA-384 digest

##### EMPTY_QUERY_BODY

The query body is empty

##### EMPTY_LIVE_HASH_QUERY

The crypto livehash query is empty

##### LIVE_HASH_NOT_FOUND

The livehash is not present

##### ACCOUNT_ID_DOES_NOT_EXIST

The account id passed has not yet been created.

##### LIVE_HASH_ALREADY_EXISTS

The livehash already exists for a given account

##### INVALID_FILE_WACL

File WACL keys are invalid

##### SERIALIZATION_FAILED

Serialization failure

##### TRANSACTION_OVERSIZE

The size of the Transaction is greater than transactionMaxBytes

##### TRANSACTION_TOO_MANY_LAYERS

The Transaction has more than 50 levels

##### CONTRACT_DELETED

Contract is marked as deleted

##### PLATFORM_NOT_ACTIVE

The platform node is either disconnected or lagging behind.

##### KEY_PREFIX_MISMATCH

One public key matches more than one prefixes on the signature map

##### PLATFORM_TRANSACTION_NOT_CREATED

Transaction not created by platform due to large backlog

##### INVALID_RENEWAL_PERIOD

Auto renewal period is not a positive number of seconds

##### INVALID_PAYER_ACCOUNT_ID

The response code when a smart contract id is passed for a crypto API request

##### ACCOUNT_DELETED

The account has been marked as deleted

##### FILE_DELETED

The file has been marked as deleted

##### ACCOUNT_REPEATED_IN_ACCOUNT_AMOUNTS

Same accounts repeated in the transfer account list

##### SETTING_NEGATIVE_ACCOUNT_BALANCE

Attempting to set negative balance value for crypto account

##### OBTAINER_REQUIRED

When deleting smart contract that has crypto balance either transfer account or transfer smart contract is required

##### OBTAINER_SAME_CONTRACT_ID

When deleting smart contract that has crypto balance you can not use the same contract id as transferContractId as the one being deleted

##### OBTAINER_DOES_NOT_EXIST

TransferAccountId or transferContractId specified for contract delete does not exist

##### MODIFYING_IMMUTABLE_CONTRACT

Attempting to modify (update or delete a immutable smart contract, i.e. one created without a admin key)

##### FILE_SYSTEM_EXCEPTION

Unexpected exception thrown by file system functions

##### AUTORENEW_DURATION_NOT_IN_RANGE

The duration is not a subset of [MINIMUM_AUTORENEW_DURATION,MAXIMUM_AUTORENEW_DURATION]

##### ERROR_DECODING_BYTESTRING

Decoding the smart contract binary to a byte array failed. Check that the input is a valid hex string.

##### CONTRACT_FILE_EMPTY

File to create a smart contract was of length zero

##### CONTRACT_BYTECODE_EMPTY

Bytecode for smart contract is of length zero

##### INVALID_INITIAL_BALANCE

Attempt to set negative initial balance

INVALID_RECEIVE_RECORD_THRESHOLD=86 [deprecated=true]; // [Deprecated]. attempt to set negative receive record threshold
INVALID_SEND_RECORD_THRESHOLD=87 [deprecated=true]; // [Deprecated]. attempt to set negative send record threshold
##### ACCOUNT_IS_NOT_GENESIS_ACCOUNT

Special Account Operations should be performed by only Genesis account, return this code if it is not Genesis Account

##### PAYER_ACCOUNT_UNAUTHORIZED

The fee payer account doesn't have permission to submit such Transaction

##### INVALID_FREEZE_TRANSACTION_BODY

FreezeTransactionBody is invalid

##### FREEZE_TRANSACTION_BODY_NOT_FOUND

FreezeTransactionBody does not exist

##### TRANSFER_LIST_SIZE_LIMIT_EXCEEDED

Exceeded the number of accounts (both from and to) allowed for crypto transfer list

##### RESULT_SIZE_LIMIT_EXCEEDED

Smart contract result size greater than specified maxResultSize

##### NOT_SPECIAL_ACCOUNT

The payer account is not a special account(account 0.0.55)

##### CONTRACT_NEGATIVE_GAS

Negative gas was offered in smart contract call

##### CONTRACT_NEGATIVE_VALUE

Negative value / initial balance was specified in a smart contract call / create

##### INVALID_FEE_FILE

Failed to update fee file

##### INVALID_EXCHANGE_RATE_FILE

Failed to update exchange rate file

##### INSUFFICIENT_LOCAL_CALL_GAS

Payment tendered for contract local call cannot cover both the fee and the gas

##### ENTITY_NOT_ALLOWED_TO_DELETE

Entities with Entity ID below 1000 are not allowed to be deleted

##### AUTHORIZATION_FAILED

Violating one of these rules: 1) treasury account can update all entities below 0.0.1000, 2) account 0.0.50 can update all entities from 0.0.51 - 0.0.80, 3) Network Function Master Account A/c 0.0.50 - Update all Network Function accounts & perform all the Network Functions listed below, 4) Network Function Accounts: i) A/c 0.0.55 - Update Address Book files (0.0.101/102), ii) A/c 0.0.56 - Update Fee schedule (0.0.111), iii) A/c 0.0.57 - Update Exchange Rate (0.0.112).

##### FILE_UPLOADED_PROTO_INVALID

Fee Schedule Proto uploaded but not valid (append or update is required)

##### FILE_UPLOADED_PROTO_NOT_SAVED_TO_DISK

Fee Schedule Proto uploaded but not valid (append or update is required)

##### FEE_SCHEDULE_FILE_PART_UPLOADED

Fee Schedule Proto File Part uploaded

##### EXCHANGE_RATE_CHANGE_LIMIT_EXCEEDED

The change on Exchange Rate exceeds Exchange_Rate_Allowed_Percentage

##### MAX_CONTRACT_STORAGE_EXCEEDED

Contract permanent storage exceeded the currently allowable limit

##### TRANSFER_ACCOUNT_SAME_AS_DELETE_ACCOUNT

Transfer Account should not be same as Account to be deleted

##### TOTAL_LEDGER_BALANCE_INVALID

No Description

##### EXPIRATION_REDUCTION_NOT_ALLOWED

The expiration date/time on a smart contract may not be reduced

##### MAX_GAS_LIMIT_EXCEEDED

Gas exceeded currently allowable gas limit per transaction

##### MAX_FILE_SIZE_EXCEEDED

File size exceeded the currently allowable limit

##### INVALID_TOPIC_ID

The Topic ID specified is not in the system.

##### INVALID_ADMIN_KEY

No Description

##### INVALID_SUBMIT_KEY

No Description

##### UNAUTHORIZED

An attempted operation was not authorized (ie - a deleteTopic for a topic with no adminKey).

##### INVALID_TOPIC_MESSAGE

A ConsensusService message is empty.

##### INVALID_AUTORENEW_ACCOUNT

The autoRenewAccount specified is not a valid, active account.

##### AUTORENEW_ACCOUNT_NOT_ALLOWED

An adminKey was not specified on the topic, so there must not be an autoRenewAccount.

##### TOPIC_EXPIRED

The topic has expired, was not automatically renewed, and is in a 7 day grace period before the topic will be deleted unrecoverably. This error response code will not be returned until autoRenew functionality is supported by HAPI.

##### INVALID_CHUNK_NUMBER

Chunk number must be from 1 to total (chunks) inclusive.

##### INVALID_CHUNK_TRANSACTION_ID

For every chunk, the payer account that is part of initialTransactionID must match the Payer Account of this transaction. The entire initialTransactionID should match the transactionID of the first chunk, but this is not checked or enforced by Hedera except when the chunk number is 1.

##### ACCOUNT_FROZEN_FOR_TOKEN

Account is frozen and cannot transact with the token

##### TOKENS_PER_ACCOUNT_LIMIT_EXCEEDED

Maximum number of token relations for agiven account is exceeded

##### INVALID_TOKEN_ID

The token is invalid or does not exist

##### INVALID_TOKEN_DECIMALS

Invalid token decimals

##### INVALID_TOKEN_INITIAL_SUPPLY

Invalid token initial supply

##### INVALID_TREASURY_ACCOUNT_FOR_TOKEN

Treasury Account does not exist or is deleted

##### INVALID_TOKEN_SYMBOL

Token Symbol is not UTF-8 capitalized alphabetical string

##### TOKEN_HAS_NO_FREEZE_KEY

Freeze key is not set on token

##### TRANSFERS_NOT_ZERO_SUM_FOR_TOKEN

Amounts in transfer list are not net zero

##### MISSING_TOKEN_SYMBOL

Token Symbol is not provided

##### TOKEN_SYMBOL_TOO_LONG

Token Symbol is too long

##### ACCOUNT_KYC_NOT_GRANTED_FOR_TOKEN

KYC must be granted and account does not have KYC granted

##### TOKEN_HAS_NO_KYC_KEY

KYC key is not set on token

##### INSUFFICIENT_TOKEN_BALANCE

Token balance is not sufficient for the transaction

##### TOKEN_WAS_DELETED

Token transactions cannot be executed on deleted token

##### TOKEN_HAS_NO_SUPPLY_KEY

Supply key is not set on token

##### TOKEN_HAS_NO_WIPE_KEY

Wipe key is not set on token

##### INVALID_TOKEN_MINT_AMOUNT

No Description

##### INVALID_TOKEN_BURN_AMOUNT

No Description

##### TOKEN_NOT_ASSOCIATED_TO_ACCOUNT

No Description

##### CANNOT_WIPE_TOKEN_TREASURY_ACCOUNT

Cannot execute wipe operation on treasury account

##### INVALID_KYC_KEY

No Description

##### INVALID_WIPE_KEY

No Description

##### INVALID_FREEZE_KEY

No Description

##### INVALID_SUPPLY_KEY

No Description

##### MISSING_TOKEN_NAME

Token Name is not provided

##### TOKEN_NAME_TOO_LONG

Token Name is too long

##### INVALID_WIPING_AMOUNT

The provided wipe amount must not be negative, zero or bigger than the token holder balance

##### TOKEN_IS_IMMUTABLE

Token does not have Admin key set, thus update/delete transactions cannot be performed

##### TOKEN_ALREADY_ASSOCIATED_TO_ACCOUNT

An <tt>associateToken</tt> operation specified a token already associated to the account

##### TRANSACTION_REQUIRES_ZERO_TOKEN_BALANCES

An attempted operation is invalid until all token balances for the target account are zero

##### ACCOUNT_IS_TREASURY

An attempted operation is invalid because the account is a treasury

##### TOKEN_ID_REPEATED_IN_TOKEN_LIST

Same TokenIDs present in the token list

##### TOKEN_TRANSFER_LIST_SIZE_LIMIT_EXCEEDED

Exceeded the number of token transfers (both from and to) allowed for token transfer list

##### EMPTY_TOKEN_TRANSFER_BODY

TokenTransfersTransactionBody has no TokenTransferList

##### EMPTY_TOKEN_TRANSFER_ACCOUNT_AMOUNTS

TokenTransfersTransactionBody has a TokenTransferList with no AccountAmounts
