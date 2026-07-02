# V2 Apps Deployments Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBEZXBsb3ltZW50cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2AppsDeploymentsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Deployments` | [`[]models.AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/an-app-deployment.md) | Optional | - |
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
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    v2AppsDeploymentsResponse := models.V2AppsDeploymentsResponse{
        Deployments:           []models.AnAppDeployment{
            models.AnAppDeployment{
                Cause:                 models.ToPointer("cause2"),
                ClonedFrom:            models.ToPointer("cloned_from4"),
                CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                Functions:             []models.FunctionsComponentsThatArePartOfThisDeployment{
                    models.FunctionsComponentsThatArePartOfThisDeployment{
                        Name:                  models.ToPointer("name4"),
                        Namespace:             models.ToPointer("namespace8"),
                        SourceCommitHash:      models.ToPointer("source_commit_hash4"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                Id:                    models.ToPointer("id6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.AnAppDeployment{
                Cause:                 models.ToPointer("cause2"),
                ClonedFrom:            models.ToPointer("cloned_from4"),
                CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                Functions:             []models.FunctionsComponentsThatArePartOfThisDeployment{
                    models.FunctionsComponentsThatArePartOfThisDeployment{
                        Name:                  models.ToPointer("name4"),
                        Namespace:             models.ToPointer("namespace8"),
                        SourceCommitHash:      models.ToPointer("source_commit_hash4"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                Id:                    models.ToPointer("id6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.AnAppDeployment{
                Cause:                 models.ToPointer("cause2"),
                ClonedFrom:            models.ToPointer("cloned_from4"),
                CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                Functions:             []models.FunctionsComponentsThatArePartOfThisDeployment{
                    models.FunctionsComponentsThatArePartOfThisDeployment{
                        Name:                  models.ToPointer("name4"),
                        Namespace:             models.ToPointer("namespace8"),
                        SourceCommitHash:      models.ToPointer("source_commit_hash4"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                Id:                    models.ToPointer("id6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Links:                 models.ToPointer(models.Links{
            Pages:                 models.ToPointer(models.LinksPagesContainer.FromPages(models.Pages{
                Last:                  models.ToPointer("last6"),
                Next:                  models.ToPointer("next2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            })),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Meta:                  models.Meta{
            Total:                 1,
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



