# Encryption Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9u

If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information.


# Class Name

`EncryptionConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EncryptionOption` | [`EncryptionOption1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/encryption-option-1.md) | Required | - |
| `KmsKey` | `string` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

EncryptionConfiguration encryptionConfiguration = new EncryptionConfiguration
{
    EncryptionOption = EncryptionOption1Enum.SSEKMS,
    KmsKey = "KmsKey6",
};
```



