# Server Backup

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlNlcnZlckJhY2t1cA

Will increase base Server costs by specific percentage


# Class Name

`ServerBackup`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Percentage` | `string` | Required | Percentage by how much the base price will increase |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serverBackup := models.ServerBackup{
        Percentage:           "20.0000000000",
    }

}
```



