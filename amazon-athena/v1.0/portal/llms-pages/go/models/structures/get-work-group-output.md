# Get Work Group Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldFdvcmtHcm91cE91dHB1dA

*This model accepts additional fields of type interface{}.*


# Class Name

`GetWorkGroupOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `WorkGroup` | [`*models.WorkGroup2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/work-group-2.md) | Optional | - |
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
    getWorkGroupOutput := models.GetWorkGroupOutput{
        WorkGroup:             models.ToPointer(models.WorkGroup2{
            Name:                  "Name2",
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
            Description:           models.ToPointer("Description4"),
            CreationTime:          models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
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



