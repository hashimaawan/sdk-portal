# Options 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRk9wdGlvbnMx

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Options1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Regions` | [`[]models.Region4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/region-4.md) | Optional | - |
| `Sizes` | [`[]models.Size1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/size-1.md) | Optional | - |
| `Versions` | [`[]models.AvailableUpgradeVersion`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/available-upgrade-version.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    options1 := models.Options1{
        Regions:               []models.Region4{
            models.Region4{
                Name:                  models.ToPointer("name0"),
                Slug:                  models.ToPointer("slug6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Sizes:                 []models.Size1{
            models.Size1{
                Name:                  models.ToPointer("name0"),
                Slug:                  models.ToPointer("slug6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Size1{
                Name:                  models.ToPointer("name0"),
                Slug:                  models.ToPointer("slug6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Versions:              []models.AvailableUpgradeVersion{
            models.AvailableUpgradeVersion{
                KubernetesVersion:     models.ToPointer("kubernetes_version6"),
                Slug:                  models.ToPointer("slug4"),
                SupportedFeatures:     []string{
                    "supported_features7",
                    "supported_features8",
                },
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



