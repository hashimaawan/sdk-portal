# Configuration Updates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNvbmZpZ3VyYXRpb25VcGRhdGVz

*This model accepts additional fields of type interface{}.*


# Class Name

`ConfigurationUpdates`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EnforceWorkGroupConfiguration` | `*bool` | Optional | - |
| `ResultConfigurationUpdates` | [`*models.ResultConfigurationUpdates2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/result-configuration-updates-2.md) | Optional | - |
| `PublishCloudWatchMetricsEnabled` | `*bool` | Optional | - |
| `BytesScannedCutoffPerQuery` | `*int` | Optional | **Constraints**: `>= 10000000` |
| `RemoveBytesScannedCutoffPerQuery` | `*bool` | Optional | - |
| `RequesterPaysEnabled` | `*bool` | Optional | - |
| `EngineVersion` | [`*models.EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/engine-version-1.md) | Optional | - |
| `RemoveCustomerContentEncryptionConfiguration` | `*bool` | Optional | - |
| `AdditionalConfiguration` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `ExecutionRole` | `*string` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `CustomerContentEncryptionConfiguration` | [`*models.CustomerContentEncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/customer-content-encryption-configuration.md) | Optional | Specifies the KMS key that is used to encrypt the user's data stores in Athena. |
| `EnableMinimumEncryptionConfiguration` | `*bool` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    configurationUpdates := models.ConfigurationUpdates{
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
    }

}
```



