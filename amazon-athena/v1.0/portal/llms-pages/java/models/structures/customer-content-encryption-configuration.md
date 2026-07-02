# Customer Content Encryption Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkN1c3RvbWVyQ29udGVudEVuY3J5cHRpb25Db25maWd1cmF0aW9u

Specifies the KMS key that is used to encrypt the user's data stores in Athena.

*This model accepts additional fields of type Object.*


# Class Name

`CustomerContentEncryptionConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `KmsKey` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:kms:([a-z0-9\-]+):\d{12}:key/?[a-zA-Z_0-9+=,.@\-_/]+$\|^arn:aws[a-z\-]*:kms:([a-z0-9\-]+):\d{12}:alias/?[a-zA-Z_0-9+=,.@\-_/]+$\|^alias/[a-zA-Z0-9/_-]+$\|[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | String getKmsKey() | setKmsKey(String kmsKey) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.CustomerContentEncryptionConfiguration;
import java.io.IOException;

CustomerContentEncryptionConfiguration customerContentEncryptionConfiguration = new CustomerContentEncryptionConfiguration.Builder(
    "KmsKey2"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



