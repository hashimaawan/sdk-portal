# V2 Apps Tiers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2AppsTiersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Tiers` | [`[]models.Tier`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/tier.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2AppsTiersResponse := models.V2AppsTiersResponse{
        Tiers:                 []models.Tier{
            models.Tier{
                BuildSeconds:          models.ToPointer("build_seconds4"),
                EgressBandwidthBytes:  models.ToPointer("egress_bandwidth_bytes2"),
                Name:                  models.ToPointer("name8"),
                Slug:                  models.ToPointer("slug8"),
                StorageBytes:          models.ToPointer("storage_bytes4"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Tier{
                BuildSeconds:          models.ToPointer("build_seconds4"),
                EgressBandwidthBytes:  models.ToPointer("egress_bandwidth_bytes2"),
                Name:                  models.ToPointer("name8"),
                Slug:                  models.ToPointer("slug8"),
                StorageBytes:          models.ToPointer("storage_bytes4"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Tier{
                BuildSeconds:          models.ToPointer("build_seconds4"),
                EgressBandwidthBytes:  models.ToPointer("egress_bandwidth_bytes2"),
                Name:                  models.ToPointer("name8"),
                Slug:                  models.ToPointer("slug8"),
                StorageBytes:          models.ToPointer("storage_bytes4"),
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



