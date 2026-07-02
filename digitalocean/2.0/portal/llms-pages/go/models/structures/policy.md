# Policy

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlBvbGljeQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Policy`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Alerts` | [`models.Alerts`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/alerts.md) | Required | - |
| `Compare` | [`models.Compare`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/compare.md) | Required | - |
| `Description` | `string` | Required | - |
| `Enabled` | `bool` | Required | - |
| `Entities` | `[]string` | Required | - |
| `Tags` | `[]string` | Required | - |
| `Type` | [`models.Type17`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/type-17.md) | Required | - |
| `Uuid` | `string` | Required | - |
| `Value` | `float64` | Required | - |
| `Window` | [`models.Window1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/window-1.md) | Required | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    policy := models.Policy{
        Alerts:                models.Alerts{
            Email:                 []string{
                "bob@exmaple.com",
            },
            Slack:                 []models.Slack{
                models.Slack{
                    Channel:               "Production Alerts",
                    Url:                   "https://hooks.slack.com/services/T1234567/AAAAAAAA/ZZZZZZ",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        Compare:               models.Compare_Greaterthan,
        Description:           "CPU Alert",
        Enabled:               true,
        Entities:              []string{
            "192018292",
        },
        Tags:                  []string{
            "droplet_tag",
        },
        Type:                  models.Type17_EnumV1Insightsdropletcpu,
        Uuid:                  "78b3da62-27e5-49ba-ac70-5db0b5935c64",
        Value:                 float64(80),
        Window:                models.Window1_Enum5M,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



