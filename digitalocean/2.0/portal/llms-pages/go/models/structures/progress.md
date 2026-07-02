# Progress

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlByb2dyZXNz

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Progress`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ErrorSteps` | `*int` | Optional | - |
| `PendingSteps` | `*int` | Optional | - |
| `RunningSteps` | `*int` | Optional | - |
| `Steps` | [`[]models.AStepThatIsRunAsPartOfTheDeploymentSLifecycle`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/a-step-that-is-run-as-part-of-the-deployment-s-lifecycle.md) | Optional | - |
| `SuccessSteps` | `*int` | Optional | - |
| `SummarySteps` | [`[]models.AStepThatIsRunAsPartOfTheDeploymentSLifecycle`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/a-step-that-is-run-as-part-of-the-deployment-s-lifecycle.md) | Optional | - |
| `TotalSteps` | `*int` | Optional | - |
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
    progress := models.Progress{
        ErrorSteps:            models.ToPointer(3),
        PendingSteps:          models.ToPointer(2),
        RunningSteps:          models.ToPointer(2),
        Steps:                 []models.AStepThatIsRunAsPartOfTheDeploymentSLifecycle{
            models.AStepThatIsRunAsPartOfTheDeploymentSLifecycle{
                ComponentName:         models.ToPointer("component_name0"),
                EndedAt:               models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                MessageBase:           models.ToPointer("message_base4"),
                Name:                  models.ToPointer("name2"),
                Reason:                models.ToPointer(models.Reason{
                    Code:                  models.ToPointer("code2"),
                    Message:               models.ToPointer("message4"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.AStepThatIsRunAsPartOfTheDeploymentSLifecycle{
                ComponentName:         models.ToPointer("component_name0"),
                EndedAt:               models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                MessageBase:           models.ToPointer("message_base4"),
                Name:                  models.ToPointer("name2"),
                Reason:                models.ToPointer(models.Reason{
                    Code:                  models.ToPointer("code2"),
                    Message:               models.ToPointer("message4"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.AStepThatIsRunAsPartOfTheDeploymentSLifecycle{
                ComponentName:         models.ToPointer("component_name0"),
                EndedAt:               models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                MessageBase:           models.ToPointer("message_base4"),
                Name:                  models.ToPointer("name2"),
                Reason:                models.ToPointer(models.Reason{
                    Code:                  models.ToPointer("code2"),
                    Message:               models.ToPointer("message4"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        SuccessSteps:          models.ToPointer(4),
        TotalSteps:            models.ToPointer(5),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



