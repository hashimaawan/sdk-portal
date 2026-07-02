# Result Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb24x


# Class Name

`ResultConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `OutputLocation` | `string` | Optional | - |
| `EncryptionConfiguration` | [`EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/encryption-configuration-2.md) | Optional | - |
| `ExpectedBucketOwner` | `string` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` |
| `AclConfiguration` | [`AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/acl-configuration-1.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

ResultConfiguration1 resultConfiguration1 = new ResultConfiguration1
{
    OutputLocation = "OutputLocation4",
    EncryptionConfiguration = new EncryptionConfiguration2
    {
        EncryptionOption = EncryptionOption1Enum.SSES3,
        KmsKey = "KmsKey6",
    },
    ExpectedBucketOwner = "ExpectedBucketOwner4",
    AclConfiguration = new AclConfiguration1
    {
        S3AclOption = S3AclOption1Enum.BUCKETOWNERFULLCONTROL,
    },
};
```



