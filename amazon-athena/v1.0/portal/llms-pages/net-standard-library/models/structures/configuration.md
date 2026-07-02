# Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNvbmZpZ3VyYXRpb24

*This model accepts additional fields of type object.*


# Class Name

`Configuration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ResultConfiguration` | [`ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/result-configuration-1.md) | Optional | - |
| `EnforceWorkGroupConfiguration` | `bool?` | Optional | - |
| `PublishCloudWatchMetricsEnabled` | `bool?` | Optional | - |
| `BytesScannedCutoffPerQuery` | `int?` | Optional | **Constraints**: `>= 10000000` |
| `RequesterPaysEnabled` | `bool?` | Optional | - |
| `EngineVersion` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/engine-version-1.md) | Optional | - |
| `AdditionalConfiguration` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `ExecutionRole` | `string` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `CustomerContentEncryptionConfiguration` | [`CustomerContentEncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/customer-content-encryption-configuration-2.md) | Optional | - |
| `EnableMinimumEncryptionConfiguration` | `bool?` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

Configuration configuration = new Configuration
{
    ResultConfiguration = new ResultConfiguration1
    {
        OutputLocation = "OutputLocation0",
        EncryptionConfiguration = new EncryptionConfiguration2
        {
            EncryptionOption = EncryptionOption1.SseS3,
            KmsKey = "KmsKey6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ExpectedBucketOwner = "ExpectedBucketOwner0",
        AclConfiguration = new AclConfiguration1
        {
            S3AclOption = S3AclOption1.BucketOwnerFullControl,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    EnforceWorkGroupConfiguration = false,
    PublishCloudWatchMetricsEnabled = false,
    BytesScannedCutoffPerQuery = 10000000,
    RequesterPaysEnabled = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



