# Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJlc291cmNlcw

An object containing additional information about resource related to a Droplet requested to be destroyed.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Resources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FloatingIps` | [`[]models.Droplet1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/droplet-1.md) | Optional | - |
| `ReservedIps` | [`[]models.Droplet1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/droplet-1.md) | Optional | - |
| `Snapshots` | [`[]models.Droplet1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/droplet-1.md) | Optional | - |
| `VolumeSnapshots` | [`[]models.Droplet1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/droplet-1.md) | Optional | - |
| `Volumes` | [`[]models.Droplet1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/droplet-1.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "digitalOceanApi/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    resources := models.Resources{
        FloatingIps:           []models.Droplet1{
            models.Droplet1{
                DestroyedAt:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                ErrorMessage:          models.ToPointer("error_message4"),
                Id:                    models.ToPointer("id2"),
                Name:                  models.ToPointer("name2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Droplet1{
                DestroyedAt:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                ErrorMessage:          models.ToPointer("error_message4"),
                Id:                    models.ToPointer("id2"),
                Name:                  models.ToPointer("name2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Droplet1{
                DestroyedAt:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                ErrorMessage:          models.ToPointer("error_message4"),
                Id:                    models.ToPointer("id2"),
                Name:                  models.ToPointer("name2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        ReservedIps:           []models.Droplet1{
            models.Droplet1{
                DestroyedAt:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                ErrorMessage:          models.ToPointer("error_message2"),
                Id:                    models.ToPointer("id0"),
                Name:                  models.ToPointer("name0"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Droplet1{
                DestroyedAt:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                ErrorMessage:          models.ToPointer("error_message2"),
                Id:                    models.ToPointer("id0"),
                Name:                  models.ToPointer("name0"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Snapshots:             []models.Droplet1{
            models.Droplet1{
                DestroyedAt:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                ErrorMessage:          models.ToPointer("error_message4"),
                Id:                    models.ToPointer("id2"),
                Name:                  models.ToPointer("name2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Droplet1{
                DestroyedAt:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                ErrorMessage:          models.ToPointer("error_message4"),
                Id:                    models.ToPointer("id2"),
                Name:                  models.ToPointer("name2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Droplet1{
                DestroyedAt:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                ErrorMessage:          models.ToPointer("error_message4"),
                Id:                    models.ToPointer("id2"),
                Name:                  models.ToPointer("name2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        VolumeSnapshots:       []models.Droplet1{
            models.Droplet1{
                DestroyedAt:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                ErrorMessage:          models.ToPointer("error_message0"),
                Id:                    models.ToPointer("id8"),
                Name:                  models.ToPointer("name8"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Droplet1{
                DestroyedAt:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                ErrorMessage:          models.ToPointer("error_message0"),
                Id:                    models.ToPointer("id8"),
                Name:                  models.ToPointer("name8"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Volumes:               []models.Droplet1{
            models.Droplet1{
                DestroyedAt:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                ErrorMessage:          models.ToPointer("error_message8"),
                Id:                    models.ToPointer("id6"),
                Name:                  models.ToPointer("name6"),
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



