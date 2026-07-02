# Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRk5vZGU

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Node`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `*time.Time` | Optional | A time value given in ISO8601 combined date and time format that represents when the node was created. |
| `DropletId` | `*string` | Optional | The ID of the Droplet used for the worker node. |
| `Id` | `*uuid.UUID` | Optional | A unique ID that can be used to identify and reference the node. |
| `Name` | `*string` | Optional | An automatically generated, human-readable name for the node. |
| `Status` | [`*models.Status10`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/status-10.md) | Optional | An object containing a `state` attribute whose value is set to a string indicating the current status of the node. |
| `UpdatedAt` | `*time.Time` | Optional | A time value given in ISO8601 combined date and time format that represents when the node was last updated. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "digitalOceanApi/models"
    "github.com/google/uuid"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    node := models.Node{
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2018-11-15T16:00:11Z", func(err error) { log.Fatalln(err) })),
        DropletId:             models.ToPointer("205545370"),
        Id:                    models.ToPointer(uuid.MustParse("e78247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f")),
        Name:                  models.ToPointer("adoring-newton-3niq"),
        Status:                models.ToPointer(models.Status10{
            State:                 models.ToPointer(models.State1_Provisioning),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        UpdatedAt:             models.ToPointer(parseTime(time.RFC3339, "2018-11-15T16:00:11Z", func(err error) { log.Fatalln(err) })),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



