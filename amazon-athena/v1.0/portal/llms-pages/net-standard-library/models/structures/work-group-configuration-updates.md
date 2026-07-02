# Work Group Configuration Updates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRldvcmtHcm91cENvbmZpZ3VyYXRpb25VcGRhdGVz

The configuration information that will be updated for this workgroup, which includes the location in Amazon S3 where query and calculation results are stored, the encryption option, if any, used for query results, whether the Amazon CloudWatch Metrics are enabled for the workgroup, whether the workgroup settings override the client-side settings, and the data usage limit for the amount of bytes scanned per query, if it is specified.

*This model accepts additional fields of type object.*


# Class Name

`WorkGroupConfigurationUpdates`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EnforceWorkGroupConfiguration` | `bool?` | Optional | - |
| `ResultConfigurationUpdates` | [`ResultConfigurationUpdates2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/result-configuration-updates-2.md) | Optional | - |
| `PublishCloudWatchMetricsEnabled` | `bool?` | Optional | - |
| `BytesScannedCutoffPerQuery` | `int?` | Optional | **Constraints**: `>= 10000000` |
| `RemoveBytesScannedCutoffPerQuery` | `bool?` | Optional | - |
| `RequesterPaysEnabled` | `bool?` | Optional | - |
| `EngineVersion` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/engine-version-1.md) | Optional | - |
| `RemoveCustomerContentEncryptionConfiguration` | `bool?` | Optional | - |
| `AdditionalConfiguration` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `ExecutionRole` | `string` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `CustomerContentEncryptionConfiguration` | [`CustomerContentEncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/customer-content-encryption-configuration.md) | Optional | Specifies the KMS key that is used to encrypt the user's data stores in Athena. |
| `EnableMinimumEncryptionConfiguration` | `bool?` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

WorkGroupConfigurationUpdates workGroupConfigurationUpdates = new WorkGroupConfigurationUpdates
{
    EnforceWorkGroupConfiguration = false,
    ResultConfigurationUpdates = new ResultConfigurationUpdates2
    {
        OutputLocation = "OutputLocation0",
        RemoveOutputLocation = false,
        EncryptionConfiguration = new EncryptionConfiguration2
        {
            EncryptionOption = EncryptionOption1.SseS3,
            KmsKey = "KmsKey6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        RemoveEncryptionConfiguration = false,
        ExpectedBucketOwner = "ExpectedBucketOwner0",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    PublishCloudWatchMetricsEnabled = false,
    BytesScannedCutoffPerQuery = 10000000,
    RemoveBytesScannedCutoffPerQuery = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



