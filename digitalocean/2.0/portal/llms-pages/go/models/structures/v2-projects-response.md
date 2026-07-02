# V2 Projects Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2ProjectsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Projects` | [`[]models.Project`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/project.md) | Optional | - |
| `Links` | [`*models.Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/links.md) | Optional | - |
| `Meta` | [`models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/meta.md) | Required | - |
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
    v2ProjectsResponse := models.V2ProjectsResponse{
        Projects:              []models.Project{
            models.Project{
                CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2018-09-27T20:10:35Z", func(err error) { log.Fatalln(err) })),
                Description:           models.ToPointer("My website API"),
                Environment:           models.ToPointer(models.Environment_Production),
                Id:                    models.ToPointer(uuid.MustParse("4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679")),
                Name:                  models.ToPointer("my-web-api"),
                OwnerId:               models.ToPointer(258992),
                OwnerUuid:             models.ToPointer("99525febec065ca37b2ffe4f852fd2b2581895e7"),
                Purpose:               models.ToPointer("Service or API"),
                UpdatedAt:             models.ToPointer(parseTime(time.RFC3339, "2018-09-27T20:10:35Z", func(err error) { log.Fatalln(err) })),
                IsDefault:             models.ToPointer(false),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Project{
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
            },
        },
        Links:                 models.ToPointer(models.Links{
            Pages:                 models.ToPointer(models.LinksPagesContainer.FromPages(models.Pages{
                Last:                  models.ToPointer("https://api.digitalocean.com/v2/projects?page=1"),
                Next:                  models.ToPointer("next2"),
                AdditionalProperties:  map[string]interface{}{
                    "first": interface{}("https://api.digitalocean.com/v2/projects?page=1"),
                },
            })),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Meta:                  models.Meta{
            Total:                 2,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



