# Update Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlVwZGF0ZVdvcmtHcm91cElucHV0

*This model accepts additional fields of type interface{}.*


# Class Name

`UpdateWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `WorkGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `ConfigurationUpdates` | [`*models.ConfigurationUpdates`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/configuration-updates.md) | Optional | - |
| `State` | [`*models.WorkGroupState2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/work-group-state-2.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    updateWorkGroupInput := models.UpdateWorkGroupInput{
        WorkGroup:             "WorkGroup0",
        Description:           models.ToPointer("Description8"),
        ConfigurationUpdates:  models.ToPointer(models.ConfigurationUpdates{
            EnforceWorkGroupConfiguration:                models.ToPointer(false),
            ResultConfigurationUpdates:                   models.ToPointer(models.ResultConfigurationUpdates2{
                OutputLocation:                models.ToPointer("OutputLocation0"),
                RemoveOutputLocation:          models.ToPointer(false),
                EncryptionConfiguration:       models.ToPointer(models.EncryptionConfiguration2{
                    EncryptionOption:      models.EncryptionOption1_SseS3,
                    KmsKey:                models.ToPointer("KmsKey6"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                RemoveEncryptionConfiguration: models.ToPointer(false),
                ExpectedBucketOwner:           models.ToPointer("ExpectedBucketOwner0"),
                AdditionalProperties:          map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            PublishCloudWatchMetricsEnabled:              models.ToPointer(false),
            BytesScannedCutoffPerQuery:                   models.ToPointer(10000000),
            RemoveBytesScannedCutoffPerQuery:             models.ToPointer(false),
            AdditionalProperties:                         map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        State:                 models.ToPointer(models.WorkGroupState2_Enabled),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



