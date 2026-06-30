# Protocol

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlByb3RvY29s

Type of traffic to allow


# Class Name

`ProtocolEnum`


# Fields

| Name |
|  --- |
| `TCP` |
| `UDP` |
| `ICMP` |
| `ESP` |
| `GRE` |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    protocol := models.ProtocolEnum_ESP

}
```



