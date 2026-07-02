# Mongodb

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRk1vbmdvZGI

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Mongodb`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Regions` | `[]string` | Optional, Read-only | An array of strings containing the names of available regions |
| `Versions` | `[]string` | Optional, Read-only | An array of strings containing the names of available regions |
| `Layouts` | [`[]models.Layout`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/layout.md) | Optional, Read-only | An array of objects, each indicating the node sizes (otherwise referred to as slugs) that are available with various numbers of nodes in the database cluster. Each slugs denotes the node's identifier, CPU, and RAM (in that order). |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    mongodb := models.Mongodb{
        Regions:               []string{
            "ams3",
            "blr1",
        },
        Versions:              []string{
            "4.4",
            "5.0",
        },
        Layouts:               []models.Layout{
            models.Layout{
                NumNodes:              models.ToPointer(190),
                Sizes:                 []string{
                    "sizes2",
                    "sizes3",
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Layout{
                NumNodes:              models.ToPointer(190),
                Sizes:                 []string{
                    "sizes2",
                    "sizes3",
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



