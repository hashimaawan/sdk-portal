# Encryption Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9uMg

*This model accepts additional fields of type object.*


# Class Name

`EncryptionConfiguration2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EncryptionOption` | [`EncryptionOption1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/encryption-option-1.md) | Required | - |
| `KmsKey` | `string` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

EncryptionConfiguration2 encryptionConfiguration2 = new EncryptionConfiguration2
{
    EncryptionOption = EncryptionOption1.SseS3,
    KmsKey = "KmsKey2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



