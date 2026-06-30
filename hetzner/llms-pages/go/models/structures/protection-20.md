# Protection 20

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlByb3RlY3Rpb24yMA

Protection configuration for the Server


# Class Name

`Protection20`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool` | Required | If true, prevents the Server from being deleted |
| `Rebuild` | `bool` | Required | If true, prevents the Server from being rebuilt |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    protection20 := models.Protection20{
        Delete:               false,
        Rebuild:              false,
    }

}
```



