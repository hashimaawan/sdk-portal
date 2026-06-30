# Storage Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlN0b3JhZ2VUeXBl

Type of Server boot drive. Local has higher speed. Network has better availability.


# Class Name

`StorageTypeEnum`


# Fields

| Name |
|  --- |
| `LOCAL` |
| `NETWORK` |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    storageType := models.StorageTypeEnum_LOCAL

}
```



