# Resources 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJlc291cmNlczM

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Resources3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ResourceId` | `*string` | Optional | The identifier of a resource. |
| `ResourceType` | [`*models.ResourceType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/resource-type-2.md) | Optional | The type of the resource. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    resources3 := models.Resources3{
        ResourceId:            models.ToPointer("3d80cb72-342b-4aaa-b92e-4e4abb24a933"),
        ResourceType:          models.ToPointer(models.ResourceType2_Volume),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



