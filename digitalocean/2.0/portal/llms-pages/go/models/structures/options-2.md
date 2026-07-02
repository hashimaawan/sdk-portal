# Options 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRk9wdGlvbnMy

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Options2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AvailableRegions` | `[]string` | Optional | - |
| `SubscriptionTiers` | [`[]models.SubscriptionTier`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/subscription-tier.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    options2 := models.Options2{
        AvailableRegions:      []string{
            "nyc3",
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
    }

}
```



