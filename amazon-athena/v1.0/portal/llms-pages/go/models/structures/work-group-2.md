# Work Group 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRldvcmtHcm91cDI

*This model accepts additional fields of type interface{}.*


# Class Name

`WorkGroup2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `State` | [`*models.WorkGroupState3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/work-group-state-3.md) | Optional | - |
| `Configuration` | [`*models.Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/configuration.md) | Optional | - |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `CreationTime` | `*time.Time` | Optional | - |
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
    workGroup2 := models.WorkGroup2{
        Name:                  "Name0",
        State:                 models.ToPointer(models.WorkGroupState3_Enabled),
        Configuration:         models.ToPointer(models.Configuration{
            ResultConfiguration:                    models.ToPointer(models.ResultConfiguration1{
                OutputLocation:          models.ToPointer("OutputLocation0"),
                EncryptionConfiguration: models.ToPointer(models.EncryptionConfiguration2{
                    EncryptionOption:      models.EncryptionOption1_SseS3,
                    KmsKey:                models.ToPointer("KmsKey6"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                ExpectedBucketOwner:     models.ToPointer("ExpectedBucketOwner0"),
                AclConfiguration:        models.ToPointer(models.AclConfiguration1{
                    S3AclOption:           models.S3AclOption1_BucketOwnerFullControl,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                AdditionalProperties:    map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            EnforceWorkGroupConfiguration:          models.ToPointer(false),
            PublishCloudWatchMetricsEnabled:        models.ToPointer(false),
            BytesScannedCutoffPerQuery:             models.ToPointer(10000000),
            RequesterPaysEnabled:                   models.ToPointer(false),
            AdditionalProperties:                   map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Description:           models.ToPointer("Description6"),
        CreationTime:          models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



