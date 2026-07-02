# V2 Projects Default Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2ProjectsDefaultResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Project` | [`*models.Project`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/project.md) | Optional | - |
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
    v2ProjectsDefaultResponse := models.V2ProjectsDefaultResponse{
        Project:               models.ToPointer(models.Project{
            CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2017-10-19T21:44:20Z", func(err error) { log.Fatalln(err) })),
            Description:           models.ToPointer("Default project"),
            Environment:           models.ToPointer(models.Environment_Development),
            Id:                    models.ToPointer(uuid.MustParse("addb4547-6bab-419a-8542-76263a033cf6")),
            Name:                  models.ToPointer("Default"),
            OwnerId:               models.ToPointer(258992),
            OwnerUuid:             models.ToPointer("99525febec065ca37b2ffe4f852fd2b2581895e7"),
            Purpose:               models.ToPointer("Just trying out DigitalOcean"),
            UpdatedAt:             models.ToPointer(parseTime(time.RFC3339, "2019-11-05T18:50:03Z", func(err error) { log.Fatalln(err) })),
            IsDefault:             models.ToPointer(true),
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



