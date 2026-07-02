# An App Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkFuJTI1MjBhcHAlMjUyMGRlcGxveW1lbnQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`AnAppDeployment`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Cause` | `*string` | Optional | - |
| `ClonedFrom` | `*string` | Optional | - |
| `CreatedAt` | `*time.Time` | Optional | - |
| `Functions` | [`[]models.FunctionsComponentsThatArePartOfThisDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/functions-components-that-are-part-of-this-deployment.md) | Optional | - |
| `Id` | `*string` | Optional | - |
| `Jobs` | [`[]models.JobComponentsThatArePartOfThisDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/job-components-that-are-part-of-this-deployment.md) | Optional | - |
| `Phase` | [`*models.Phase`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/phase.md) | Optional | **Default**: `"UNKNOWN"` |
| `PhaseLastUpdatedAt` | `*time.Time` | Optional | - |
| `Progress` | [`*models.Progress`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/progress.md) | Optional | - |
| `Services` | [`[]models.ServiceComponentsThatArePartOfThisDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/service-components-that-are-part-of-this-deployment.md) | Optional | - |
| `Spec` | [`*models.AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/app-spec.md) | Optional | The desired configuration of an application. |
| `StaticSites` | [`[]models.StaticSiteComponentsThatArePartOfThisDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/static-site-components-that-are-part-of-this-deployment.md) | Optional | - |
| `TierSlug` | `*string` | Optional, Read-only | - |
| `UpdatedAt` | `*time.Time` | Optional | - |
| `Workers` | [`[]models.WorkerComponentsThatArePartOfThisDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/worker-components-that-are-part-of-this-deployment.md) | Optional | - |
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
    anAppDeployment := models.AnAppDeployment{
        Cause:                 models.ToPointer("commit 9a4df0b pushed to github/digitalocean/sample-golang"),
        ClonedFrom:            models.ToPointer("3aa4d20e-5527-4c00-b496-601fbd22520a"),
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-07-28T18:00:00Z", func(err error) { log.Fatalln(err) })),
        Functions:             []models.FunctionsComponentsThatArePartOfThisDeployment{
            models.FunctionsComponentsThatArePartOfThisDeployment{
                Name:                  models.ToPointer("name4"),
                Namespace:             models.ToPointer("namespace8"),
                SourceCommitHash:      models.ToPointer("source_commit_hash4"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.FunctionsComponentsThatArePartOfThisDeployment{
                Name:                  models.ToPointer("name4"),
                Namespace:             models.ToPointer("namespace8"),
                SourceCommitHash:      models.ToPointer("source_commit_hash4"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Id:                    models.ToPointer("b6bdf840-2854-4f87-a36c-5f231c617c84"),
        Phase:                 models.ToPointer(models.Phase_Active),
        PhaseLastUpdatedAt:    models.ToPointer(parseTime(time.RFC3339, "0001-01-01T00:00:00Z", func(err error) { log.Fatalln(err) })),
        TierSlug:              models.ToPointer("basic"),
        UpdatedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-07-28T18:00:00Z", func(err error) { log.Fatalln(err) })),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



