# `enum HbarUnit`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`TINYBAR`](#tinybar) | ✅ | ✅ | ✅
| [`MICROBAR`](#microbar) | ✅ | ✅ | ✅
| [`MILLIBAR`](#millibar) | ✅ | ✅ | ✅
| [`HBAR`](#hbar) | ✅ | ✅ | ✅
| [`KILOBAR`](#kilobar) | ✅ | ✅ | ✅
| [`MEGABAR`](#megabar) | ✅ | ✅ | ✅
| [`GIGABAR`](#gigabar) | ✅ | ✅ | ✅
| [`toString()`](#tostring) | ✅ | ✅ | ✅

## Variants

### `TINYBAR`

The atomic (smallest) unit of hbar, used natively by the Hedera network.
It is equivalent to <sup>1</sup>&frasl;<sub>100,000,000</sub> hbar.

```typescript
TINYBAR(symbol: "tℏ", tinybar: 1)
```

### `MICROBAR`

Equivalent to 100 tinybar or <sup>1</sup>&frasl;<sub>1,000,000</sub> hbar.

```typescript
MICROBAR(symbol: "μℏ", tinybar: 100)
```

### `MILLIBAR`

Equivalent to 100,000 tinybar or <sup>1</sup>&frasl;<sub>1,000</sub> hbar.
```typescript
MILLIBAR(symbol: "mℏ", tinybar: 100_000)
```

### `HBAR`

The base unit of hbar, equivalent to 100 million tinybar.
```typescript
HBAR(symbol: "ℏ", tinybar: 100_000_000)
```

### `KILOBAR`

Equivalent to 1 thousand hbar or 100 billion tinybar.

```typescript
KILOBAR(symbol: "kℏ", tinybar: 1000 * 100_000_000L)
```

### `MEGABAR`

Equivalent to 1 million hbar or 100 trillion tinybar.

```typescript
MEGABAR(symbol: "Mℏ", tinybar: 1_000_000 * 100_000_000L)
```

### `GIGABAR`

Equivalent to 1 billion hbar or 100 quadillion tinybar.

```typescript
MEGABAR(symbol: "Gℏ", tinybar: 1_000_000_000 * 100_000_000L)
```

## Methods

### `toString()`

```typescript
toString(): string
```
