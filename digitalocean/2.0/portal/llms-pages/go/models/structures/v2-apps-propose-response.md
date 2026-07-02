# V2 Apps Propose Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBQcm9wb3NlJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2AppsProposeResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AppCost` | `*int` | Optional | The monthly cost of the proposed app in USD using the next pricing plan tier. For example, if you propose an app that uses the Basic tier, the `app_tier_upgrade_cost` field displays the monthly cost of the app if it were to use the Professional tier. If the proposed app already uses the most expensive tier, the field is empty. |
| `AppIsStatic` | `*bool` | Optional | Indicates whether the app is a static app. |
| `AppNameAvailable` | `*bool` | Optional | Indicates whether the app name is available. |
| `AppNameSuggestion` | `*string` | Optional | The suggested name if the proposed app name is unavailable. |
| `AppTierDowngradeCost` | `*int` | Optional | The monthly cost of the proposed app in USD using the previous pricing plan tier. For example, if you propose an app that uses the Professional tier, the `app_tier_downgrade_cost` field displays the monthly cost of the app if it were to use the Basic tier. If the proposed app already uses the lest expensive tier, the field is empty. |
| `ExistingStaticApps` | `*string` | Optional | The maximum number of free static apps the account can have. We will charge you for any additional static apps. |
| `Spec` | [`*models.AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/app-spec.md) | Optional | The desired configuration of an application. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2AppsProposeResponse := models.V2AppsProposeResponse{
        AppCost:               models.ToPointer(5),
        AppIsStatic:           models.ToPointer(true),
        AppNameAvailable:      models.ToPointer(true),
        AppNameSuggestion:     models.ToPointer("newName"),
        AppTierDowngradeCost:  models.ToPointer(17),
        ExistingStaticApps:    models.ToPointer("2"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



