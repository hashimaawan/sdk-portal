# Work Group Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRldvcmtHcm91cFN1bW1hcnk

The summary information for the workgroup, which includes its name, state, description, and the date and time it was created.


# Class Name

`WorkGroupSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `*string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `State` | [`*models.WorkGroupState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/work-group-state-1.md) | Optional | - |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `CreationTime` | `*time.Time` | Optional | - |
| `EngineVersion` | [`*models.EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/engine-version-1.md) | Optional | - |


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
    workGroupSummary := models.WorkGroupSummary{
        Name:                 models.ToPointer("Name4"),
        State:                models.ToPointer(models.WorkGroupState1Enum_ENABLED),
        Description:          models.ToPointer("Description8"),
        CreationTime:         models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        EngineVersion:        models.ToPointer(models.EngineVersion1{
            SelectedEngineVersion:  models.ToPointer("SelectedEngineVersion4"),
            EffectiveEngineVersion: models.ToPointer("EffectiveEngineVersion6"),
        }),
    }

}
```



