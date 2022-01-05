> `JsonRpcSignatureProvider` implements `SignatureProvider`

JSON RPC Signature providers **MUST** implement [JSON RPC](https://www.jsonrpc.org/specification)

The `params` type is defined in [JSON RPC Definitions](#jsonrpcdefinitions)

### Static Methods

##### `fromUrl` ( `url`: `string` ): `JsonSignatureProvider`

Creates an `JsonSignatureProvider` for a gRPC server.

---

### Methods

##### async `getPublicKeys` (): `List` < `PublicKey` >

Lists all the public keys which will sign the requests

##### async `sign` ( `messages`: `List` < `bytes` > ): `List` < `List` < `SignatureProviderSignature` > >

Signs all the messages.

---

##### `toString` (): `string`

Outputs `[JsonSignatureProvider] <url>`

---

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

interface GetPublicKeysMethodRequest {
    jsonrpc: "2.0",
    method: "getPublicKeys",
}

interface GetPublicKeysMethodResponse {
    jsonrpc: "2.0",
    result?: GetPublicKeyResponse,
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
     * Each key **MUST** be an ASN.1 encoded public key
     */
    publicKeys: Uint8Array[];

    /**
     * **MUST NOT** repeat the `Signature.public_key` multiple types otherwise the RPC will be
     * considered failed and all signatures disgarded.
     *
     * Each element in this list **MUST** match the signatures for the interface at the same index.
     */
    signatures: SignatureList[];
}

/**
 * List of sigantures for a given interfaces
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

/**
 * Lists all the public keys
 *
 * Strictlly declared to hopefully future proof
 */
interface GetPublicKeyResponse = GetPublicKeyResponseV1;

interface GetPublicKeyResponseV1 {
    /**
     * Each key **MUST** be an ASN.1 encoded public key
     */
    publicKeys: Uint8Array[];
}
```
