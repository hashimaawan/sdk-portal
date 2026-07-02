# V2 Apps Alerts Destinations Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBBbGVydHMlMjUyMERlc3RpbmF0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2AppsAlertsDestinationsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Alert` | [`*models.Alert1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/alert-1.md) | Optional | - |
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
    v2AppsAlertsDestinationsResponse := models.V2AppsAlertsDestinationsResponse{
        Alert:                 models.ToPointer(models.Alert1{
            ComponentName:         models.ToPointer("component_name2"),
            Emails:                []string{
                "emails9",
            },
            Id:                    models.ToPointer("id0"),
            Phase:                 models.ToPointer(models.Phase1_Configuring),
            Progress:              models.ToPointer(models.Progress2{
                Steps:                 []models.StepsOfAnAlertSProgress{
                    models.StepsOfAnAlertSProgress{
                        EndedAt:               models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                        Name:                  models.ToPointer("name2"),
                        Reason:                models.ToPointer(models.Reason{
                            Code:                  models.ToPointer("code2"),
                            Message:               models.ToPointer("message4"),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        }),
                        StartedAt:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                        Status:                models.ToPointer(models.Status2_Success),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                    models.StepsOfAnAlertSProgress{
                        EndedAt:               models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                        Name:                  models.ToPointer("name2"),
                        Reason:                models.ToPointer(models.Reason{
                            Code:                  models.ToPointer("code2"),
                            Message:               models.ToPointer("message4"),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        }),
                        StartedAt:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                        Status:                models.ToPointer(models.Status2_Success),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                    models.StepsOfAnAlertSProgress{
                        EndedAt:               models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                        Name:                  models.ToPointer("name2"),
                        Reason:                models.ToPointer(models.Reason{
                            Code:                  models.ToPointer("code2"),
                            Message:               models.ToPointer("message4"),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        }),
                        StartedAt:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                        Status:                models.ToPointer(models.Status2_Success),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
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



