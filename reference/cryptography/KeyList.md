# class `KeyList`

A list of Keys (`Key`) with an optional threshold.

This class implements the collection interface of the
implementation language and thus can look very different between each SDK.

## Fields

### `threshold: int`

A threshold indicating that a valid signature set must have at least
this many signatures.

## Static Methods

### `constructor()`

Create a new, empty list of keys with no threshold.

### `withThreshold(threshold: int): KeyList`

Create a new, empty list of keys with the given threshold.

## Declaration

```typescript
class KeyList extends Array<Key> {
    constructor();

    static withThreshold(threshold: int): KeyList;

    threshold: int;
}
```

## Examples

#### Java

```java
var keyList = new KeyList();
keyList.threshold = 1;
keyList.add(keyA);
keyList.add(keyB);

myAccountCreateTransaction.setKey(keyList);
```

#### JavaScript

```javascript
const keyList = KeyList.of(keyA, keyB);
keyList.threshold = 1;

myAccountCreateTransaction.setKey(keyList);
```

#### Go

```go
keyList := NewKeyListWith(keyA, keyB)
keyList.Threshold = 1

myAccountCreateTransaction.SetKey(keyList)
```
