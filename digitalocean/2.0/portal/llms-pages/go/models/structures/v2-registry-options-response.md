# V2 Registry Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwT3B0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2RegistryOptionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Options` | [`*models.Options2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/options-2.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2RegistryOptionsResponse := models.V2RegistryOptionsResponse{
        Options:               models.ToPointer(models.Options2{
            AvailableRegions:      []string{
                "available_regions9",
            },
            SubscriptionTiers:     []models.SubscriptionTier{
                models.SubscriptionTier{
                    AllowStorageOverage:        models.ToPointer(false),
                    IncludedBandwidthBytes:     models.ToPointer(int64(172)),
                    IncludedRepositories:       models.ToPointer(194),
                    IncludedStorageBytes:       models.ToPointer(int64(242)),
                    MonthlyPriceInCents:        models.ToPointer(236),
                    AdditionalProperties:       map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.SubscriptionTier{
                    AllowStorageOverage:        models.ToPointer(false),
                    IncludedBandwidthBytes:     models.ToPointer(int64(172)),
                    IncludedRepositories:       models.ToPointer(194),
                    IncludedStorageBytes:       models.ToPointer(int64(242)),
                    MonthlyPriceInCents:        models.ToPointer(236),
                    AdditionalProperties:       map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.SubscriptionTier{
                    AllowStorageOverage:        models.ToPointer(false),
                    IncludedBandwidthBytes:     models.ToPointer(int64(172)),
                    IncludedRepositories:       models.ToPointer(194),
                    IncludedStorageBytes:       models.ToPointer(int64(242)),
                    MonthlyPriceInCents:        models.ToPointer(236),
                    AdditionalProperties:       map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



