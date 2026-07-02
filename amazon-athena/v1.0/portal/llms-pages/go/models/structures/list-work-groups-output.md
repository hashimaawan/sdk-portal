# List Work Groups Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RXb3JrR3JvdXBzT3V0cHV0

*This model accepts additional fields of type interface{}.*


# Class Name

`ListWorkGroupsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `WorkGroups` | [`[]models.WorkGroupSummary`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/work-group-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `50` |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "amazonAthena/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    listWorkGroupsOutput := models.ListWorkGroupsOutput{
        WorkGroups:            []models.WorkGroupSummary{
            models.WorkGroupSummary{
                Name:                  models.ToPointer("Name4"),
                State:                 models.ToPointer(models.WorkGroupState1_Enabled),
                Description:           models.ToPointer("Description0"),
                CreationTime:          models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                EngineVersion:         models.ToPointer(models.EngineVersion1{
                    SelectedEngineVersion:  models.ToPointer("SelectedEngineVersion4"),
                    EffectiveEngineVersion: models.ToPointer("EffectiveEngineVersion6"),
                    AdditionalProperties:   map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.WorkGroupSummary{
                Name:                  models.ToPointer("Name4"),
                State:                 models.ToPointer(models.WorkGroupState1_Enabled),
                Description:           models.ToPointer("Description0"),
                CreationTime:          models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                EngineVersion:         models.ToPointer(models.EngineVersion1{
                    SelectedEngineVersion:  models.ToPointer("SelectedEngineVersion4"),
                    EffectiveEngineVersion: models.ToPointer("EffectiveEngineVersion6"),
                    AdditionalProperties:   map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.WorkGroupSummary{
                Name:                  models.ToPointer("Name4"),
                State:                 models.ToPointer(models.WorkGroupState1_Enabled),
                Description:           models.ToPointer("Description0"),
                CreationTime:          models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                EngineVersion:         models.ToPointer(models.EngineVersion1{
                    SelectedEngineVersion:  models.ToPointer("SelectedEngineVersion4"),
                    EffectiveEngineVersion: models.ToPointer("EffectiveEngineVersion6"),
                    AdditionalProperties:   map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        NextToken:             models.ToPointer("NextToken2"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



