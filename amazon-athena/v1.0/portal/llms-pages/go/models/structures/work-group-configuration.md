# Work Group Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRldvcmtHcm91cENvbmZpZ3VyYXRpb24

The configuration of the workgroup, which includes the location in Amazon S3 where query and calculation results are stored, the encryption option, if any, used for query and calculation results, whether the Amazon CloudWatch Metrics are enabled for the workgroup and whether workgroup settings override query settings, and the data usage limits for the amount of data scanned per query or per workgroup. The workgroup settings override is specified in <code>EnforceWorkGroupConfiguration</code> (true/false) in the <code>WorkGroupConfiguration</code>. See <a>WorkGroupConfiguration$EnforceWorkGroupConfiguration</a>.

*This model accepts additional fields of type interface{}.*


# Class Name

`WorkGroupConfiguration`


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
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    workGroupConfiguration := models.WorkGroupConfiguration{
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
    }

}
```



