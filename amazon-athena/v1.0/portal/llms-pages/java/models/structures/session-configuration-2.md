# Session Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlNlc3Npb25Db25maWd1cmF0aW9uMg

*This model accepts additional fields of type Object.*


# Class Name

`SessionConfiguration2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ExecutionRole` | `String` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` | String getExecutionRole() | setExecutionRole(String executionRole) |
| `WorkingDirectory` | `String` | Optional | - | String getWorkingDirectory() | setWorkingDirectory(String workingDirectory) |
| `IdleTimeoutSeconds` | `Integer` | Optional | - | Integer getIdleTimeoutSeconds() | setIdleTimeoutSeconds(Integer idleTimeoutSeconds) |
| `EncryptionConfiguration` | [`EncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/encryption-configuration.md) | Optional | If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information. | EncryptionConfiguration getEncryptionConfiguration() | setEncryptionConfiguration(EncryptionConfiguration encryptionConfiguration) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration;
import com.amazonaws.useast1.athena.models.EncryptionOption1;
import com.amazonaws.useast1.athena.models.SessionConfiguration2;
import java.io.IOException;

SessionConfiguration2 sessionConfiguration2 = new SessionConfiguration2.Builder()
    .executionRole("ExecutionRole0")
    .workingDirectory("WorkingDirectory4")
    .idleTimeoutSeconds(82)
    .encryptionConfiguration(new EncryptionConfiguration.Builder(
        EncryptionOption1.SSE_S3
    )
    .kmsKey("KmsKey6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



