# V2 Droplets Destroy with Associated Resources Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTdGF0dXMlMjUyMFJlc3BvbnNl

An objects containing information about a resources scheduled for deletion.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CompletedAt` | `*time.Time` | Optional | A time value given in ISO8601 combined date and time format indicating when the requested action was completed. |
| `Droplet` | [`*models.Droplet1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/droplet-1.md) | Optional | An object containing information about a resource scheduled for deletion. |
| `Failures` | `*int` | Optional | A count of the associated resources that failed to be destroyed, if any. |
| `Resources` | [`*models.Resources`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/resources.md) | Optional | An object containing additional information about resource related to a Droplet requested to be destroyed. |
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
    v2DropletsDestroyWithAssociatedResourcesStatusResponse := models.V2DropletsDestroyWithAssociatedResourcesStatusResponse{
        CompletedAt:           models.ToPointer(parseTime(time.RFC3339, "2020-04-01T18:11:49Z", func(err error) { log.Fatalln(err) })),
        Droplet:               models.ToPointer(models.Droplet1{
            DestroyedAt:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            ErrorMessage:          models.ToPointer("error_message2"),
            Id:                    models.ToPointer("id0"),
            Name:                  models.ToPointer("name0"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Failures:              models.ToPointer(0),
        Resources:             models.ToPointer(models.Resources{
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
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



