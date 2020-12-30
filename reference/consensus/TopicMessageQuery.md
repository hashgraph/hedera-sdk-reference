# `TopicMessageQuery`

## Support

| [`constructor()`](#constructor) | ✅ | ✅ | ✅
| [`setTopicId()`](#settopicid) | ✅ | ✅ | ✅
| [`setStartTime()`](#setstarttime) | ✅ | ✅ | ✅
| [`setEndTime()`](#setendtime) | ✅ | ✅ | ✅
| [`setLimit()`](#setlimit) | ✅ | ✅ | ✅
| [`subscribe()`](#subscribe) | ✅ | ✅ | ✅
| [`execute()`](#execute) | ✅ | ✅ | ✅
| [`setNodeId()`](#setnodeid) | ✅ | ✅ | ✅
| [`getNodeId()`](#getnodeid) | ✅ | ✅ | ✅
| [`setQueryPayment()`](#setquerypayment) | ✅ | ✅ | ✅
| [`setMaxQueryPayment()`](#setmaxquerypayment) | ✅ | ✅ | ✅
| [`getCost()`](#getcost) | ✅ | ✅ | ✅
| [`toBytes()`](#tobytes) | ✅ | ✅ | ✅
| [`fromBytes()`](#frombytes) | ✅ | ✅ | ✅

## Methods

### `constructor()`

```typescript
constructor()
```

### `setTopicId()`

```typescript
setTopicId(id: TopicId): this
```

### `setStartTime()`

```typescript
setStartTime(time: Timestamp): this
```

### `setEndTime()`

```typescript
setEndTime(time: Timestamp): this
```

### `setLimit()`

```typescript
setLimit(limit: long): this
```

### `subscribe()`

```typescript
subscribe(
    client: Client,
    onNext: Consumer<TopicMessage>): SubscriptionHandle
```

### `execute()`

```typescript
async execute(client: Client): this
```

### `setNodeId()`

```typescript
setNodeId(id: AccountId): this
```

### `getNodeId()`

```typescript
getNodeId(): AccountId
```

### `setQueryPayment()`

```typescript
setQueryPayment(payment: Hbar): this
```

### `setMaxQueryPayment()`

```typescript
setMaxQueryPayment(payment: Hbar): this
```

### `getCost()`

```typescript
async getCost(client: Client): Hbar
```

### `toBytes()`

```typescript
toBytes(): bytes
```

### `fromBytes()`

```typescript
fromBytes(data: bytes): this
```
