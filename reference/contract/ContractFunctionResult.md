> class `ContractFunctionResult`

### Properties

##### `contractId`: [`ContractId`](reference/contract/ContractId.md)

The smart contract instance whose function was called

---

##### `errorMessage`: `String`

Message In case there was an error during smart contract execution

---

##### `bloom`: `bytes`

Bloom filter for record

---

##### `gasUsed`: `Uint64`

Units of gas used to execute contract

---

##### `logs`: `List` < [`ContractLogInfo`](reference/contract/ContractLogInfo.md) >

The log info for events returned by the function

---

##### `createdContractIds`: `List` < [`ContractId`](reference/contract/ContractId.md) >

The list of smart contracts that were created by the function call
[DEPRECATED] the list of smart contracts that were created by the function call.

The created ids will now _also_ be externalized through internal transaction 
records, where each record has its alias field populated with the new contract's 
EVM address. (This is needed for contracts created with CREATE2, since 
there is no longer a simple relationship between the new contract's 0.0.X id 
and its Solidity address.)

---

##### `stateChanges`: `List` < [`ContractStateChange`](reference/contract/ContractStateChange.md) >

The list of state reads and changes caused by this function call

---

##### `evmAddress`: [`ContractId`](reference/contract/ContractId.md)

The contracts evm address represented as a contract ID with `ContractId.evmAddress` set accordingly.

---

### Methods

##### `asBytes` ( ): `bytes`

---

##### `getString` ( `index`: `Uint64` ): `String`

---

##### `getStringArray` ( `index`: `Uint64` ): `String[]`

---

##### `getBytes` ( `index`: `Uint64` ): `bytes`

---

##### `getBytes32` ( `index`: `Uint64` ): `bytes`

---

##### `getDynamicBytes` ( `index`: `Uint64` ): `bytes`

---

##### `getBool` ( `index`: `Uint64` ): `bool`

---

##### `getInt8` ( `index`: `Uint64` ): `Int8`

---

##### `getInt32` ( `index`: `Uint64` ): `Int32`

---

##### `getInt64` ( `index`: `Uint64` ): `Int64`

---

##### `getInt256` ( `index`: `Uint64` ): `BigInteger`

---

##### `getUint8` ( `index`: `Uint64` ): `Uint8`

---

##### `getUint32` ( `index`: `Uint64` ): `Uint32`

---

##### `getUint64` ( `index`: `Uint64` ): `Uint64`

---

##### `getUint256` ( `index`: `Uint64` ): `BigInteger`

---

##### `getAddress` ( `index`: `Uint64` ): `string`

---
