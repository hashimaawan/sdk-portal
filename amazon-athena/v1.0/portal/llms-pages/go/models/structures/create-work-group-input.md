# Create Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZVdvcmtHcm91cElucHV0

*This model accepts additional fields of type interface{}.*


# Class Name

`CreateWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `Configuration` | [`*models.Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/configuration.md) | Optional | - |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `Tags` | [`[]models.Tag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/tag.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    createWorkGroupInput := models.CreateWorkGroupInput{
        Name:                  "Name6",
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
        Description:           models.ToPointer("Description0"),
        Tags:                  []models.Tag{
            models.Tag{
                Key:                   models.ToPointer("Key0"),
                Value:                 models.ToPointer("Value6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Tag{
                Key:                   models.ToPointer("Key0"),
                Value:                 models.ToPointer("Value6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



