# Servers Actions Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwVHlwZSUyNTIwUmVxdWVzdA


# Class Name

`ServersActionsChangeTypeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ServerType` | `string` | Required | ID or name of Server type the Server should migrate to |
| `UpgradeDisk` | `bool` | Required | If false, do not upgrade the disk (this allows downgrading the Server type later) |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serversActionsChangeTypeRequest := models.ServersActionsChangeTypeRequest{
        ServerType:           "cx11",
        UpgradeDisk:          true,
    }

}
```



