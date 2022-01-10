> class `JsonRpcProvider` extends `Provider`

JSON RPC Signature providers **MUST** implement [JSON RPC](https://www.jsonrpc.org/specification)

The `params` type is defined in [JSON RPC Definitions](#jsonrpcdefinitions)

### JSON RPC Defintions

```typescript
interface SignMethodRequest {
    jsonrpc: "2.0",
    method: "sign",
    params: SignRequest,
}

interface SignMethodResponse {
    jsonrpc: "2.0",
    result?: SignResponse,
    error?: JsonRpcError,
    id: string | number | null;
}

interface JsonRpcError {
    code: number;
    message: string;
    data?: any;
}

/**
 * Strictlly declared to hopefully future proof
 */
interface SignRequest = ResponseSignatureV1;

/**
 * Strictlly declared to hopefully future proof
 */
interface SignResponse = ResponseSignatureV1;

/**
 * A simple request to sign a interface
 */
interface RequestSignatureV1 {
    /**
     * Each interface that needs to be signed
     */
    interfaces: Uint8Array[];
}

/**
 * Strictlly declared to hopefully future proof
 */
interface ResponseSignatureV1 {
    /**
     * Each key **MUST** be an SPKI DER encoded public key
     */
    publicKeys: Uint8Array[];

    /**
     * **MUST NOT** repeat the `Signature.publicKey` multiple types otherwise the RPC will be
     * considered failed and all signatures disgarded.
     *
     * Each element in this list **MUST** match the signatures for the public key at the same index.
     *
     * e.g. The signatures for the message at index 0 will be accessible 
     * `ResponseSignatureV1.signatures[0].signatures`
     */
    signatures: SignatureList[];
}

/**
 * List of sigantures for a given messages
 */
interface SignatureList {
    signatures: Signature[];
}

/**
 * The signature for particular interface and public key
 *
 * **NOTE**: The reasoning for using indices is to shink the response size when
 * multiple keys and interfaces are used.
 */
interface Signature {
    /**
     * The index of the public key in the response
     */
    publicKeyIndex: number;

    signature: Uint8Array;
}
