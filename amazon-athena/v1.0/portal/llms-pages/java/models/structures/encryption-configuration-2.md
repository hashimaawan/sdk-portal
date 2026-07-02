# Encryption Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9uMg

*This model accepts additional fields of type Object.*


# Class Name

`EncryptionConfiguration2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `EncryptionOption` | [`EncryptionOption1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/encryption-option-1.md) | Required | - | EncryptionOption1 getEncryptionOption() | setEncryptionOption(EncryptionOption1 encryptionOption) |
| `KmsKey` | `String` | Optional | - | String getKmsKey() | setKmsKey(String kmsKey) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1;
import java.io.IOException;

EncryptionConfiguration2 encryptionConfiguration2 = new EncryptionConfiguration2.Builder(
    EncryptionOption1.SSE_S3
)
.kmsKey("KmsKey2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



