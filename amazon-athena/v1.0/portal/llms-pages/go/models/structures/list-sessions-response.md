# List Sessions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1Jlc3BvbnNl


# Class Name

`ListSessionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NextToken` | `*string` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `Sessions` | [`[]models.SessionSummary`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/session-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` |


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
    listSessionsResponse := models.ListSessionsResponse{
        NextToken:            models.ToPointer("NextToken6"),
        Sessions:             []models.SessionSummary{
            models.SessionSummary{
                SessionId:            models.ToPointer("SessionId6"),
                Description:          models.ToPointer("Description4"),
                EngineVersion:        models.ToPointer(models.EngineVersion1{
                    SelectedEngineVersion:  models.ToPointer("SelectedEngineVersion4"),
                    EffectiveEngineVersion: models.ToPointer("EffectiveEngineVersion6"),
                }),
                NotebookVersion:      models.ToPointer("NotebookVersion6"),
                Status:               models.ToPointer(models.Status3{
                    StartDateTime:        models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    LastModifiedDateTime: models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    EndDateTime:          models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    IdleSinceDateTime:    models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    State:                models.ToPointer(models.SessionState1Enum_TERMINATING),
                }),
            },
            models.SessionSummary{
                SessionId:            models.ToPointer("SessionId6"),
                Description:          models.ToPointer("Description4"),
                EngineVersion:        models.ToPointer(models.EngineVersion1{
                    SelectedEngineVersion:  models.ToPointer("SelectedEngineVersion4"),
                    EffectiveEngineVersion: models.ToPointer("EffectiveEngineVersion6"),
                }),
                NotebookVersion:      models.ToPointer("NotebookVersion6"),
                Status:               models.ToPointer(models.Status3{
                    StartDateTime:        models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    LastModifiedDateTime: models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    EndDateTime:          models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    IdleSinceDateTime:    models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    State:                models.ToPointer(models.SessionState1Enum_TERMINATING),
                }),
            },
            models.SessionSummary{
                SessionId:            models.ToPointer("SessionId6"),
                Description:          models.ToPointer("Description4"),
                EngineVersion:        models.ToPointer(models.EngineVersion1{
                    SelectedEngineVersion:  models.ToPointer("SelectedEngineVersion4"),
                    EffectiveEngineVersion: models.ToPointer("EffectiveEngineVersion6"),
                }),
                NotebookVersion:      models.ToPointer("NotebookVersion6"),
                Status:               models.ToPointer(models.Status3{
                    StartDateTime:        models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    LastModifiedDateTime: models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    EndDateTime:          models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    IdleSinceDateTime:    models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    State:                models.ToPointer(models.SessionState1Enum_TERMINATING),
                }),
            },
        },
    }

}
```



