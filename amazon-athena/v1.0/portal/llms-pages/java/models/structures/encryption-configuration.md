# Encryption Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9u

If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information.


# Class Name

`EncryptionConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `EncryptionOption` | [`EncryptionOption1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/encryption-option-1.md) | Required | - | EncryptionOption1Enum getEncryptionOption() | setEncryptionOption(EncryptionOption1Enum encryptionOption) |
| `KmsKey` | `String` | Optional | - | String getKmsKey() | setKmsKey(String kmsKey) |


# Example

```java
import com.amazonaws.useast1.athena.models.EncryptionConfiguration;
import com.amazonaws.useast1.athena.models.EncryptionOption1Enum;

EncryptionConfiguration encryptionConfiguration = new EncryptionConfiguration.Builder(
    EncryptionOption1Enum.SSE_KMS
)
.kmsKey("KmsKey6")
.build();
```



