# Node Selection

### Why

Selecting which nodes to use for a request is incredibly important selecting poorly 
performing nodes will result in a bad experience and slow or failing requests.

### Node Health

#### Variables to consider

- [`useCount`] Number of times it was used: fewer is better
- [`lastUsed`] The last time it was used: earlier is better
- [`badGrpcStatusCount`] Number of bad gRPC status received: less is better
- [`currentBackoff`] Current backoff: less is better

#### Comparison

 - Compare the nodes [`currentBackoff`]
    - Return node with lower value or proceed if equal
 - Compare the nodes [`badGrpcStatusCount`]
    - Return node with lower value or proceed if equal
 - Compare the nodes [`useCount`]
    - Return node with lower value or proceed if equal
 - Compare the nodes [`lastUsed`]
    - Return node with lower value or proceed if equal
 - Nodes have same health, so they're treated as equal


```javascript
/**
 * @param {Node} a
 * @param {Node} b
 * @returns {number}
 */
function compare(a, b) {
    if (a.currentBackoff < b.currentBackoff) {
        return -1;
    } else if (b.currentBackoff < a.currentBackoff) {
        return 1;
    }

    if (a.badGrpcStatusCount < b.badGrpcStatusCount) {
        return -1;
    } else if (b.badGrpcStatusCount < a.badGrpcStatusCount) {
        return 1;
    }

    if (a.useCount < b.useCount) {
        return -1;
    } else if (b.useCount < a.useCount) {
        return 1;
    }

    if (a.lastUsed < b.lastUsed) {
        return -1;
    } else if (b.lastUsed < a.lastUsed) {
        return 1;
    }

    return 0;
}
```

```java
public static int compare(Node a, Node b) {
    if (a.currentBackoff < b.currentBackoff) {
        return -1;
    } else if (b.currentBackoff < a.currentBackoff) {
        return 1;
    }

    if (a.badGrpcStatusCount < b.badGrpcStatusCount) {
        return -1;
    } else if (b.badGrpcStatusCount < a.badGrpcStatusCount) {
        return 1;
    }

    if (a.useCount < b.useCount) {
        return -1;
    } else if (b.useCount < a.useCount) {
        return 1;
    }

    if (a.lastUsed < b.lastUsed) {
        return -1;
    } else if (b.lastUsed < a.lastUsed) {
        return 1;
    }

    return 0;
}
```

```go
func compare(a Node, b Node) int {
    if (a.currentBackoff < b.currentBackoff) {
        return -1
    } else if (b.currentBackoff < a.currentBackoff) {
        return 1
    }

    if (a.badGrpcStatusCount < b.badGrpcStatusCount) {
        return -1
    } else if (b.badGrpcStatusCount < a.badGrpcStatusCount) {
        return 1
    }

    if (a.useCount < b.useCount) {
        return -1
    } else if (b.useCount < a.useCount) {
        return 1
    }

    if (a.lastUsed < b.lastUsed) {
        return -1
    } else if (b.lastUsed < a.lastUsed) {
        return 1
    }

    return 0;
}
```
