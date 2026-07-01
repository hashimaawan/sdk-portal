# Servers Actions Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwVHlwZSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type interface{}.*


# Class Name

`ServersActionsChangeTypeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ServerType` | `string` | Required | ID or name of Server type the Server should migrate to |
| `UpgradeDisk` | `bool` | Required | If false, do not upgrade the disk (this allows downgrading the Server type later) |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    serversActionsChangeTypeRequest := models.ServersActionsChangeTypeRequest{
        ServerType:            "cx11",
        UpgradeDisk:           true,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



