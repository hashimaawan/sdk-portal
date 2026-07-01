# Server Backup

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlckJhY2t1cA

Will increase base Server costs by specific percentage

*This model accepts additional fields of type interface{}.*


# Class Name

`ServerBackup`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Percentage` | `string` | Required | Percentage by how much the base price will increase |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    serverBackup := models.ServerBackup{
        Percentage:            "20.0000000000",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



