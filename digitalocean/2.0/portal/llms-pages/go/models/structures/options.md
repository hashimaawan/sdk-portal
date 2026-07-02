# Options

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRk9wdGlvbnM

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Options`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Mongodb` | [`*models.Mongodb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/mongodb.md) | Optional | - |
| `Mysql` | [`*models.Mysql`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/mysql.md) | Optional | - |
| `Pg` | [`*models.Pg`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/pg.md) | Optional | - |
| `Redis` | [`*models.Redis`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/redis.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    options := models.Options{
        Mongodb:               models.ToPointer(models.Mongodb{
            Regions:               []string{
                "regions3",
                "regions4",
            },
            Versions:              []string{
                "versions3",
                "versions4",
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
        }),
        Mysql:                 models.ToPointer(models.Mysql{
            Regions:               []string{
                "regions9",
                "regions0",
                "regions1",
            },
            Versions:              []string{
                "versions9",
                "versions0",
                "versions1",
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
        }),
        Pg:                    models.ToPointer(models.Pg{
            Regions:               []string{
                "regions3",
            },
            Versions:              []string{
                "versions3",
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
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Redis:                 models.ToPointer(models.Redis{
            Regions:               []string{
                "regions7",
            },
            Versions:              []string{
                "versions7",
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



