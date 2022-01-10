> class `GrpcSignatureProvider` extends `provider`

### Protobuf Defintions

```protobuf
/**
 * Strictlly declared to hopefully future proof
 */
message SignRequest {
    oneof versions {
        RequestSignatureV1 v1 = 1;
    }
}

/**
 * Strictlly declared to hopefully future proof
 */
message SignResponse {
    oneof versions {
        ResponseSignatureV1 v1 = 1;
    }
}

/**
 * A simple request to sign a message
 */
message RequestSignatureV1 {
    /**
     * Each message that needs to be signed
     */
    repeated bytes messages = 1;
}

/**
 * Strictlly declared to hopefully future proof
 */
message ResponseSignatureV1 {
    /**
     * Each key **MUST** be an SPKI DER encoded public key
     */
    repeated bytes public_keys = 1;

    /**
     * **MUST NOT** repeat the `Signature.public_key` multiple types otherwise the RPC will be
     * considered failed and all signatures disgarded.
     *
     * Each element in this list **MUST** match the signatures for the message at the same index.
     */
    repeated SignatureList signatures = 1;
}

/**
 * List of sigantures for a given messages
 */
message SignatureList {
    repeated Signature signatures = 1;
}

/**
 * The signature for particular message and public key
 *
 * **NOTE**: The reasoning for using indices is to shink the response size when
 * multiple keys and messages are used.
 */
message Signature {
    /**
     * The index of the public key in the response
     */
    uint32 public_key_index = 1;

    bytes signature = 2;
}

/**
 * The gRPC API for signing
 */
service GrpcSignatureProvider {
    rpc sign(SignRequest) SignResponse
}
```
