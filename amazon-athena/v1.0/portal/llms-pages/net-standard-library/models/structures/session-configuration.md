# Session Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlc3Npb25Db25maWd1cmF0aW9u

Contains session configuration information.


# Class Name

`SessionConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExecutionRole` | `string` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `WorkingDirectory` | `string` | Optional | - |
| `IdleTimeoutSeconds` | `int?` | Optional | - |
| `EncryptionConfiguration` | [`EncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/encryption-configuration.md) | Optional | If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information. |


# Example

```csharp
using AmazonAthena.Standard.Models;

SessionConfiguration sessionConfiguration = new SessionConfiguration
{
    ExecutionRole = "ExecutionRole2",
    WorkingDirectory = "WorkingDirectory6",
    IdleTimeoutSeconds = 188,
    EncryptionConfiguration = new EncryptionConfiguration
    {
        EncryptionOption = EncryptionOption1Enum.SSES3,
        KmsKey = "KmsKey6",
    },
};
```



