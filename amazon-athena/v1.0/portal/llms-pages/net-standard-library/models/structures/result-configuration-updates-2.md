# Result Configuration Updates 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb25VcGRhdGVzMg

*This model accepts additional fields of type object.*


# Class Name

`ResultConfigurationUpdates2`


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

ResultConfigurationUpdates2 resultConfigurationUpdates2 = new ResultConfigurationUpdates2
{
    OutputLocation = "OutputLocation4",
    RemoveOutputLocation = false,
    EncryptionConfiguration = new EncryptionConfiguration2
    {
        EncryptionOption = EncryptionOption1.SseS3,
        KmsKey = "KmsKey6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    RemoveEncryptionConfiguration = false,
    ExpectedBucketOwner = "ExpectedBucketOwner4",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



