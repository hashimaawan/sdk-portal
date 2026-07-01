# Direction

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkRpcmVjdGlvbg

Select traffic direction on which rule should be applied. Use `source_ips` for direction `in` and `destination_ips` for direction `out`.


# Class Name

`DirectionEnum`


# Fields

| Name |
|  --- |
| `IN` |
| `OUT` |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    direction := models.DirectionEnum_IN

}
```



