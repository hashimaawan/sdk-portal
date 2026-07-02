# V2 Databases Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9wdGlvbnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DatabasesOptionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Options` | [`*models.Options`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/options.md) | Optional | - |
| `VersionAvailability` | [`*models.VersionAvailability`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/version-availability.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2DatabasesOptionsResponse := models.V2DatabasesOptionsResponse{
        Options:               models.ToPointer(models.Options{
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
        }),
        VersionAvailability:   models.ToPointer(models.VersionAvailability{
            Mongodb:               []models.Mongodb1{
                models.Mongodb1{
                    EndOfAvailability:     models.ToPointer("end_of_availability4"),
                    EndOfLife:             models.ToPointer("end_of_life4"),
                    Version:               models.ToPointer("version4"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Mongodb1{
                    EndOfAvailability:     models.ToPointer("end_of_availability4"),
                    EndOfLife:             models.ToPointer("end_of_life4"),
                    Version:               models.ToPointer("version4"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Mysql:                 []models.Mongodb1{
                models.Mongodb1{
                    EndOfAvailability:     models.ToPointer("end_of_availability0"),
                    EndOfLife:             models.ToPointer("end_of_life0"),
                    Version:               models.ToPointer("version0"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Mongodb1{
                    EndOfAvailability:     models.ToPointer("end_of_availability0"),
                    EndOfLife:             models.ToPointer("end_of_life0"),
                    Version:               models.ToPointer("version0"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Pg:                    []models.Mongodb1{
                models.Mongodb1{
                    EndOfAvailability:     models.ToPointer("end_of_availability4"),
                    EndOfLife:             models.ToPointer("end_of_life4"),
                    Version:               models.ToPointer("version4"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Redis:                 []models.Mongodb1{
                models.Mongodb1{
                    EndOfAvailability:     models.ToPointer("end_of_availability8"),
                    EndOfLife:             models.ToPointer("end_of_life8"),
                    Version:               models.ToPointer("version8"),
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



