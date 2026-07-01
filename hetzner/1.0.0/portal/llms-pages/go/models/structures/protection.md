# Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByb3RlY3Rpb24

Protection configuration for the Resource


# Class Name

`Protection`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool` | Required | If true, prevents the Resource from being deleted |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    protection := models.Protection{
        Delete:               false,
    }

}
```



