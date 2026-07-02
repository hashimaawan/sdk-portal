# Session Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlc3Npb25Db25maWd1cmF0aW9uMg

*This model accepts additional fields of type object.*


# Class Name

`SessionConfiguration2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExecutionRole` | `string` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `WorkingDirectory` | `string` | Optional | - |
| `IdleTimeoutSeconds` | `int?` | Optional | - |
| `EncryptionConfiguration` | [`EncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/encryption-configuration.md) | Optional | If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

SessionConfiguration2 sessionConfiguration2 = new SessionConfiguration2
{
    ExecutionRole = "ExecutionRole0",
    WorkingDirectory = "WorkingDirectory4",
    IdleTimeoutSeconds = 82,
    EncryptionConfiguration = new EncryptionConfiguration
    {
        EncryptionOption = EncryptionOption1.SseS3,
        KmsKey = "KmsKey6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



