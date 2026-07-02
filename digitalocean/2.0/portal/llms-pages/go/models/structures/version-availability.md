# Version Availability

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlZlcnNpb25BdmFpbGFiaWxpdHk

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`VersionAvailability`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Mongodb` | [`[]models.Mongodb1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `Mysql` | [`[]models.Mongodb1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `Pg` | [`[]models.Mongodb1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `Redis` | [`[]models.Mongodb1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    versionAvailability := models.VersionAvailability{
        Mongodb:               []models.Mongodb1{
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
        Redis:                 []models.Mongodb1{
            models.Mongodb1{
                EndOfAvailability:     models.ToPointer("end_of_availability8"),
                EndOfLife:             models.ToPointer("end_of_life8"),
                Version:               models.ToPointer("version8"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
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
    }

}
```



