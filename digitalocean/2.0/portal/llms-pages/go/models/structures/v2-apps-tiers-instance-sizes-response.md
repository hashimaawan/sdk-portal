# V2 Apps Tiers Instance Sizes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwSW5zdGFuY2UlMjUyMFNpemVzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2AppsTiersInstanceSizesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DiscountPercent` | `*float64` | Optional | - |
| `InstanceSizes` | [`[]models.InstanceSize`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/instance-size.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2AppsTiersInstanceSizesResponse := models.V2AppsTiersInstanceSizesResponse{
        DiscountPercent:       models.ToPointer(float64(2.32)),
        InstanceSizes:         []models.InstanceSize{
            models.InstanceSize{
                CpuType:               models.ToPointer(models.MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores_Dedicated),
                Cpus:                  models.ToPointer("cpus4"),
                MemoryBytes:           models.ToPointer("memory_bytes8"),
                Name:                  models.ToPointer("name8"),
                Slug:                  models.ToPointer("slug8"),
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



