# List Work Groups Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RXb3JrR3JvdXBzT3V0cHV0


# Class Name

`ListWorkGroupsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `WorkGroups` | [`[]models.WorkGroupSummary`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/work-group-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `50` |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```go
package main

import (
    "log"
    "time"
    "amazonathena/models"
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
        WorkGroups:           []models.WorkGroupSummary{
            models.WorkGroupSummary{
                Name:                 models.ToPointer("Name4"),
                State:                models.ToPointer(models.WorkGroupState1Enum_ENABLED),
                Description:          models.ToPointer("Description0"),
                CreationTime:         models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                EngineVersion:        models.ToPointer(models.EngineVersion1{
                    SelectedEngineVersion:  models.ToPointer("SelectedEngineVersion4"),
                    EffectiveEngineVersion: models.ToPointer("EffectiveEngineVersion6"),
                }),
            },
            models.WorkGroupSummary{
                Name:                 models.ToPointer("Name4"),
                State:                models.ToPointer(models.WorkGroupState1Enum_ENABLED),
                Description:          models.ToPointer("Description0"),
                CreationTime:         models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                EngineVersion:        models.ToPointer(models.EngineVersion1{
                    SelectedEngineVersion:  models.ToPointer("SelectedEngineVersion4"),
                    EffectiveEngineVersion: models.ToPointer("EffectiveEngineVersion6"),
                }),
            },
            models.WorkGroupSummary{
                Name:                 models.ToPointer("Name4"),
                State:                models.ToPointer(models.WorkGroupState1Enum_ENABLED),
                Description:          models.ToPointer("Description0"),
                CreationTime:         models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                EngineVersion:        models.ToPointer(models.EngineVersion1{
                    SelectedEngineVersion:  models.ToPointer("SelectedEngineVersion4"),
                    EffectiveEngineVersion: models.ToPointer("EffectiveEngineVersion6"),
                }),
            },
        },
        NextToken:            models.ToPointer("NextToken2"),
    }

}
```



