# Encryption Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9u

If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information.

*This model accepts additional fields of type Object.*


# Class Name

`EncryptionConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `EncryptionOption` | [`EncryptionOption1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/encryption-option-1.md) | Required | - | EncryptionOption1 getEncryptionOption() | setEncryptionOption(EncryptionOption1 encryptionOption) |
| `KmsKey` | `String` | Optional | - | String getKmsKey() | setKmsKey(String kmsKey) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration;
import com.amazonaws.useast1.athena.models.EncryptionOption1;
import java.io.IOException;

EncryptionConfiguration encryptionConfiguration = new EncryptionConfiguration.Builder(
    EncryptionOption1.SSE_KMS
)
.kmsKey("KmsKey6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



