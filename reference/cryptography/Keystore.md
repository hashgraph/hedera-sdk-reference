# `Keystore`

> class `Keystore`


<details>
<summary><b>Table of Contents</b></summary>

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`constructor()`](#constructor-key-privatekey-) | ✅ | ✅ | ✅
| [`fromStream()`](#fromstream-input-inputstream-passphrase-string-keystore) | ✅ | ✅ | ✅
| [`getEd25519()`](#geted25519-privatekey) | ✅ | ✅ | ✅
| [`export()`](#export-output-outputstream-passphrase-string-) | ✅ | ✅ | ✅
</details>

<!-- tabs:start -->

###### ** Java **

```java
var privateKey = PrivateKey.generate();
var keystore = new Keystore(privateKey);
```

### ** JavaScript **

```javascript
const key = PrivateKey.generate()
const keystore = await key.toKeystore()

const keystore = createKeystore(key.toBytes(), passphrase);
```

###### ** Go **

```go
privateKey, err := hedera.GeneratePrivateKey()
if err != nil {
    println(err.Error())
}

keyStore, err := hedera.newKeystore(privateKey.Bytes(), passphrase)
if err != nil {
    println(err.Error())
}

ksPrivateKey, err := hedera.parseKeystore(keyStore, passphrase)
if err != nil {
    println(err.Error())
}
```

<!-- tabs:end -->

### Constructor

##### `constructor`( `key`: `PrivateKey` )

---

### Static Methods

##### `fromStream` ( `input`: `InputStream`, `passphrase`: `String` ): `Keystore`

---

### Methods

##### `getEd25519` (): [`PrivateKey`](/reference/cryptography/PrivateKey.md)

---

##### `export` ( `output`: `OutputStream`, `passphrase`: `String` )

---
