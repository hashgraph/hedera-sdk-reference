# interface `Key`

## Implementors

 * [`PublicKey`](PublicKey.md)

 * [`PrivateKey`](PrivateKey.md)

 * [`KeyList`](KeyList.md)

## Static Methods

### `fromBytes(data: bytes): Key`

Parses a PublicKey, PrivateKey, or KeyList from bytes.

## Methods

### `toBytes(): bytes`

Converts this key into bytes.

## Declaration

```typescript
interface Key {
    static fromBytes(data: bytes): Key;

    toBytes(): bytes;
}
```
