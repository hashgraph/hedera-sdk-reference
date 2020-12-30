# `Hbar`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`ZERO`](#zero) | ✅ | ✅ | ✅
| [`MAX`](#max) | ✅ | ✅ | ✅
| [`MIN`](#min) | ✅ | ✅ | ✅
| [`fromString()`](#fromstring) | ✅ | ✅ | ✅
| [`from()`](#from) | ✅ | ✅ | ✅
| [`fromTinybars()`](#fromtinybars) | ✅ | ✅ | ✅
| [`toTinybars()`](#totinybars) | ✅ | ✅ | ✅
| [`to()`](#to) | ✅ | ✅ | ✅
| [`getValue()`](#getValue) | ✅ | ✅ | ✅
| [`negated()`](#negated) | ✅ | ✅ | ✅
| [`equals()`](#equals) | ✅ | ✅ | ✅
| [`compareTo()`](#compareto) | ✅ | ✅ | ✅

## Constants

### `ZERO`

A constant value of zero hbars.

```typescript
ZERO: this
```

### `MAX`

A constant value of the maximum number of hbars.

```typescript
MAX: this
```

### `MIN`

A constant value of the minimum number of hbars.

```typescript
MIN: this
```

## Methods

### `constructor()`

```typescript
costructor(amount: long | amount: BigDecimal)
```

### `fromString()`

```typescript
fromString(
    text: CharSequence
    | text: CharSequence, unit: HbarUnit): this
```

### `from()`

```typescript
from(
    hbars: long
    | amount: long, unit: HbarUnit
    | hbars: BigDecimal
    | amount: BigDecimal, unit: HbarUnit): this
```

### `fromTinybars()`

```typescript
fromTinybars(tinybars: long): this
```

### `toTinybars()`

```typescript
toTinybars(): long
```

### `to()`

```typescript
to(unit: HbarUnit): BigDecimal
```

### `getValue()`

```typescript
getValue(): BigDecimal
```

### `negated()`

```typescript
negated(): this
```

### `equals()`

```typescript
equals(o: Object): boolean
```

### `compareTo()`

```typescript
compareTo(hbar: Hbar): int
```
