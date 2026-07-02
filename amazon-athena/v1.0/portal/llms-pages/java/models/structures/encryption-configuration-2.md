# Encryption Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9uMg


# Class Name

`EncryptionConfiguration2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `EncryptionOption` | [`EncryptionOption1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/encryption-option-1.md) | Required | - | EncryptionOption1Enum getEncryptionOption() | setEncryptionOption(EncryptionOption1Enum encryptionOption) |
| `KmsKey` | `String` | Optional | - | String getKmsKey() | setKmsKey(String kmsKey) |


# Example

```java
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1Enum;

EncryptionConfiguration2 encryptionConfiguration2 = new EncryptionConfiguration2.Builder(
    EncryptionOption1Enum.SSE_S3
)
.kmsKey("KmsKey2")
.build();
```



