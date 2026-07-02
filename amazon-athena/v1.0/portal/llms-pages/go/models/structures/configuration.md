# Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNvbmZpZ3VyYXRpb24


# Class Name

`Configuration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ResultConfiguration` | [`*models.ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/result-configuration-1.md) | Optional | - |
| `EnforceWorkGroupConfiguration` | `*bool` | Optional | - |
| `PublishCloudWatchMetricsEnabled` | `*bool` | Optional | - |
| `BytesScannedCutoffPerQuery` | `*int` | Optional | **Constraints**: `>= 10000000` |
| `RequesterPaysEnabled` | `*bool` | Optional | - |
| `EngineVersion` | [`*models.EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/engine-version-1.md) | Optional | - |
| `AdditionalConfiguration` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `ExecutionRole` | `*string` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `CustomerContentEncryptionConfiguration` | [`*models.CustomerContentEncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/customer-content-encryption-configuration-2.md) | Optional | - |
| `EnableMinimumEncryptionConfiguration` | `*bool` | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    configuration := models.Configuration{
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
    }

}
```



