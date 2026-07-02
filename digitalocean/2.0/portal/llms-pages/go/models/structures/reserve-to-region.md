# Reserve to Region

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJlc2VydmUlMjUyMHRvJTI1MjBSZWdpb24

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`ReserveToRegion`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ProjectId` | `*uuid.UUID` | Optional | The UUID of the project to which the floating IP will be assigned. |
| `Region` | `string` | Required | The slug identifier for the region the floating IP will be reserved to. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
    "github.com/google/uuid"
)

func main() {
    reserveToRegion := models.ReserveToRegion{
        ProjectId:             models.ToPointer(uuid.MustParse("746c6152-2fa2-11ed-92d3-27aaa54e4988")),
        Region:                "nyc3",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



