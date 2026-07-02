# Encryption Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9uMg


# Class Name

`EncryptionConfiguration2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EncryptionOption` | [`EncryptionOption1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/encryption-option-1.md) | Required | - |
| `KmsKey` | `string` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

EncryptionConfiguration2 encryptionConfiguration2 = new EncryptionConfiguration2
{
    EncryptionOption = EncryptionOption1Enum.SSES3,
    KmsKey = "KmsKey2",
};
```



