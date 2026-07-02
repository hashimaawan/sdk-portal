# Subscription Tier

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlN1YnNjcmlwdGlvblRpZXI

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`SubscriptionTier`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AllowStorageOverage` | `*bool` | Optional | A boolean indicating whether the subscription tier supports additional storage above what is included in the base plan at an additional cost per GiB used. |
| `IncludedBandwidthBytes` | `*int64` | Optional | The amount of outbound data transfer included in the subscription tier in bytes. |
| `IncludedRepositories` | `*int` | Optional | The number of repositories included in the subscription tier. `0` indicates that the subscription tier includes unlimited repositories. |
| `IncludedStorageBytes` | `*int64` | Optional | The amount of storage included in the subscription tier in bytes. |
| `MonthlyPriceInCents` | `*int` | Optional | The monthly cost of the subscription tier in cents. |
| `Name` | `*string` | Optional | The name of the subscription tier. |
| `Slug` | `*string` | Optional | The slug identifier of the subscription tier. |
| `StorageOveragePriceInCents` | `*int` | Optional | The price paid in cents per GiB for additional storage beyond what is included in the subscription plan. |
| `EligibilityReasons` | [`[]models.EligibilityReason`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/eligibility-reason.md) | Optional | If your account is not eligible to use a certain subscription tier, this will include a list of reasons that prevent you from using the tier. |
| `Eligible` | `*bool` | Optional | A boolean indicating whether your account it eligible to use a certain subscription tier. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    subscriptionTier := models.SubscriptionTier{
        AllowStorageOverage:        models.ToPointer(true),
        IncludedBandwidthBytes:     models.ToPointer(int64(5368709120)),
        IncludedRepositories:       models.ToPointer(5),
        IncludedStorageBytes:       models.ToPointer(int64(5368709120)),
        MonthlyPriceInCents:        models.ToPointer(500),
        Name:                       models.ToPointer("Basic"),
        Slug:                       models.ToPointer("basic"),
        StorageOveragePriceInCents: models.ToPointer(2),
        EligibilityReasons:         []models.EligibilityReason{
            models.EligibilityReason_Overrepositorylimit,
        },
        Eligible:                   models.ToPointer(true),
        AdditionalProperties:       map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



