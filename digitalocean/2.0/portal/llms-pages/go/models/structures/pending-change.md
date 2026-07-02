# Pending Change

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlBlbmRpbmdDaGFuZ2U

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`PendingChange`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DropletId` | `*int` | Optional | - |
| `Removing` | `*bool` | Optional | - |
| `Status` | `*string` | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    pendingChange := models.PendingChange{
        DropletId:             models.ToPointer(8043964),
        Removing:              models.ToPointer(false),
        Status:                models.ToPointer("waiting"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



