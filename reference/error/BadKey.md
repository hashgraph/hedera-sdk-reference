# `BadKey`

> error `BadKey`

<details>
<summary><b>Declaration</b></summary>

```typescript
class BadKeyError extends Error {}
```

</details>

Signals that a private or public key could not be realized from the input.

- `PrivateKey.fromString`
- `PrivateKey.fromPem`
- `PrivateKey.fromBytes`
- `PrivateKey.fromKeystore`
- `PublicKey.fromString`
- `PublicKey.fromBytes`
