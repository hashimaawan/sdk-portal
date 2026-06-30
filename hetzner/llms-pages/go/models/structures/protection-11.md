# Protection 11

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlByb3RlY3Rpb24xMQ

Protection configuration for the Network


# Class Name

`Protection11`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool` | Required | If true, prevents the Network from being deleted |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    protection11 := models.Protection11{
        Delete:               false,
    }

}
```



