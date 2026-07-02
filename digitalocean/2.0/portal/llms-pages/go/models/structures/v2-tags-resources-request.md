# V2 Tags Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjBSZXNvdXJjZXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2TagsResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Resources` | [`[]models.Resources3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/resources-3.md) | Required | An array of objects containing resource_id and resource_type  attributes. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2TagsResourcesRequest := models.V2TagsResourcesRequest{
        Resources:             []models.Resources3{
            models.Resources3{
                ResourceId:            models.ToPointer("9569411"),
                ResourceType:          models.ToPointer(models.ResourceType2_Droplet),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Resources3{
                ResourceId:            models.ToPointer("7555620"),
                ResourceType:          models.ToPointer(models.ResourceType2_Image),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Resources3{
                ResourceId:            models.ToPointer("3d80cb72-342b-4aaa-b92e-4e4abb24a933"),
                ResourceType:          models.ToPointer(models.ResourceType2_Volume),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



