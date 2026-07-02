# Create Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZVdvcmtHcm91cElucHV0


# Class Name

`CreateWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `Configuration` | [`*models.Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/configuration.md) | Optional | - |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `Tags` | [`[]models.Tag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/tag.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    createWorkGroupInput := models.CreateWorkGroupInput{
        Name:                 "Name6",
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
        Description:          models.ToPointer("Description0"),
        Tags:                 []models.Tag{
            models.Tag{
                Key:                  models.ToPointer("Key0"),
                Value:                models.ToPointer("Value6"),
            },
            models.Tag{
                Key:                  models.ToPointer("Key0"),
                Value:                models.ToPointer("Value6"),
            },
        },
    }

}
```



