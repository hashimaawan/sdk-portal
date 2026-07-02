# Result Configuration Updates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb25VcGRhdGVz

The information about the updates in the query results, such as output location and encryption configuration for the query results.

*This model accepts additional fields of type object.*


# Class Name

`ResultConfigurationUpdates`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `OutputLocation` | `string` | Optional | - |
| `RemoveOutputLocation` | `bool?` | Optional | - |
| `EncryptionConfiguration` | [`EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/encryption-configuration-2.md) | Optional | - |
| `RemoveEncryptionConfiguration` | `bool?` | Optional | - |
| `ExpectedBucketOwner` | `string` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` |
| `RemoveExpectedBucketOwner` | `bool?` | Optional | - |
| `AclConfiguration` | [`AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/acl-configuration-1.md) | Optional | - |
| `RemoveAclConfiguration` | `bool?` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

ResultConfigurationUpdates resultConfigurationUpdates = new ResultConfigurationUpdates
{
    OutputLocation = "OutputLocation6",
    RemoveOutputLocation = false,
    EncryptionConfiguration = new EncryptionConfiguration2
    {
        EncryptionOption = EncryptionOption1.SseS3,
        KmsKey = "KmsKey6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    RemoveEncryptionConfiguration = false,
    ExpectedBucketOwner = "ExpectedBucketOwner6",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



