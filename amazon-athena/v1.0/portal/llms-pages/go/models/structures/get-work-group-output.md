# Get Work Group Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldFdvcmtHcm91cE91dHB1dA


# Class Name

`GetWorkGroupOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `WorkGroup` | [`*models.WorkGroup2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/work-group-2.md) | Optional | - |


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
    getWorkGroupOutput := models.GetWorkGroupOutput{
        WorkGroup:            models.ToPointer(models.WorkGroup2{
            Name:                 "Name2",
            State:                models.ToPointer(models.WorkGroupState3Enum_ENABLED),
            Configuration:        models.ToPointer(models.Configuration{
                ResultConfiguration:                    models.ToPointer(models.ResultConfiguration1{
                    OutputLocation:          models.ToPointer("OutputLocation0"),
                    EncryptionConfiguration: models.ToPointer(models.EncryptionConfiguration2{
                        EncryptionOption:     models.EncryptionOption1Enum_SSES3,
                        KmsKey:               models.ToPointer("KmsKey6"),
                    }),
                    ExpectedBucketOwner:     models.ToPointer("ExpectedBucketOwner0"),
                    AclConfiguration:        models.ToPointer(models.AclConfiguration1{
                        S3AclOption:          models.S3AclOption1Enum_BUCKETOWNERFULLCONTROL,
                    }),
                }),
                EnforceWorkGroupConfiguration:          models.ToPointer(false),
                PublishCloudWatchMetricsEnabled:        models.ToPointer(false),
                BytesScannedCutoffPerQuery:             models.ToPointer(10000000),
                RequesterPaysEnabled:                   models.ToPointer(false),
            }),
            Description:          models.ToPointer("Description4"),
            CreationTime:         models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        }),
    }

}
```



