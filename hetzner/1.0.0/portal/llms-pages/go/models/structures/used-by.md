# Used By

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlVzZWRCeQ


# Class Name

`UsedBy`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `int` | Required | ID of resource referenced |
| `Type` | `string` | Required | Type of resource referenced |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    usedBy := models.UsedBy{
        Id:                   4711,
        Type:                 "load_balancer",
    }

}
```



