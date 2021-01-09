# `KeyList`

> class `KeyList` extends `Collection<Key>` implements [`Key`](reference/cryptography/Key.md)

<details>
<summary><b>Declaration</b></summary>

```typescript
class KeyList extends Collection<Key> implements Key {
    /* property */ threshold: Uint;
}
```

</details>

A list of Keys (`Key`) with an optional threshold.

This class implements the collection interface of the
implementation language and thus can look very different between each SDK.

A `KeyList` can be used anywhere that a `Key` is expected in the SDK. This
includes `setKey` in `AccountCreateTransaction` and `setSubmitKey` in
`TopicCreateTransaction`.

<!-- tabs:start -->

### ** Java **

```java
// imperative
var keyList = KeyList.withThreshold(1);
keyList.add(keyA);
keyList.add(keyB);

// fluid
var keyList = KeyList.of(keyA, keyB).setThreshold(1);
```

### ** JavaScript **

```javascript
// imperative
const keyList = KeyList.withThreshold(1);
keyList.add(key1);
keyList.addAll(List.of(key2, key3));

// fluid
const keyList = KeyList.of(keyA, keyB).setThreshold(1);
```

### ** Go **

```go
// imperative
keyList := NewKeyList()
keyList = keyList.SetThreshold(1)
keyList = keyList.Append(keyA)
keyList = keyList.Append(keyB)

// from array
keyList := NewKeyListFromSlice([]{
    keyA,
    keyB,
}).SetThreshold(1)

// fluid
keyList := NewKeyListWith(keyA, keyB).SetThreshold(1)
```

### ** Python **

```python
# imperative
key_list = KeyList(threshold=1)
key_list.append(key_a)
key_list.append(key_b)

# from array
key_list = KeyList([key_a, key_b], threshold=1)
```

<!-- tabs:end -->

### Constructor

##### `constructor` ()

Create a new, empty list of keys with no threshold.

### Static Methods

##### `withThreshold` ( `threshold`: `Uint` ): `KeyList`

Create a new, empty list of keys with the given threshold.

---

##### `of` (`keyArray` : `Key[]`): `KeyList`

---

### Methods


##### `isEmpty` (): `bool`

---

##### `contains` (`keys` : `KeyList`): `bool`

---

##### `iterator` (): `Iterator<Key>`

---

##### `add` (`key` : `Key`): `bool`

---

##### `remove` (`keyList` : `KeyList`): `bool`

---

##### `clear` ()

---

##### `equals` (`keyList` : `KeyList`): `bool`

---

##### `hashCode` (): `int`

---

##### `toString` (): `String`

---

### Properties

### `threshold`: `Uint`

A threshold indicating that a valid signature set must have at least
this many signatures.
