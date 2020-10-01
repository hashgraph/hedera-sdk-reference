# `Hbar`

## Support

| Item | Java | JavaScript | Go
| - | - | - | - |
| [`ZERO`](#zero) | ✅ | ✅ | O
| [`MAX`](#max) | ✅ | ✅ | O
| [`MIN`](#min) | ✅ | ✅ | O
| [`fromString()`](#fromstring) | ✅ | ✅ | O
| [`from()`](#from) | ✅ | ✅ | O
| [`fromTinybars()`](#fromtinybars) | ✅ | ✅ | O
| [`toTinybars()`](#totinybars) | ✅ | ✅ | O
| [`to()`](#to) | ✅ | ✅ | O
| [`getValue()`](#getValue) | ✅ | ✅ | O
| [`negated()`](#negated) | ✅ | ✅ | O
| [`equals()`](#equals) | ✅ | ✅ | O
| [`hashCode()`](#hashcode) | ✅ | ✅ | O
| [`compareTo()`](#compareto) | ✅ | ✅ | O

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

### `hashCode()`

```typescript
hashCode(): int
```

### `compareTo()`

```typescript
compareTo(hbar: Hbar): int
```