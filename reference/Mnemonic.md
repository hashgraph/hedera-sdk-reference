# `Mnemonic`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`words`](#words) | ✅ | ✅ | O
| [`fromWords()`](#fromwords) | ✅ | ✅ | O
| [`fromString()`](#fromstring) | ✅ | ✅ | O
| [`generate24()`](#generate24) | ✅ | ✅ | O
| [`generate12()`](#generate12) | ✅ | ✅ | O
| [`toPrivateKey()`](#toprivatekey) | ✅ | ✅ | O

## Fields

### `words`

```typescript
words: List<CharSequence>
```

## Methods

### `fromWords()`

```typescript
fromWords(words: List<CharSequence>): this
```

### `fromString()`

```typescript
fromString(mnemonic: string): this
```

### `generate24()`

```typescript
generate24(): this
```

### `generate12()`

```typescript
generate12(): this
```

### `toPrivateKey()`

```typescript
toPrivateKey(passphrase: string): PrivateKey
```

### `toPrivateKey()`

```typescript
toPrivateKey(): PrivateKey
```