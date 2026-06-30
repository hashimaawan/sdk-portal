# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlJlc291cmNl


# Class Name

`Resource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `int` | Required | ID of the Resource |
| `Type` | `string` | Required | Type of resource referenced |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    resource := models.Resource{
        Id:                   42,
        Type:                 "server",
    }

}
```



