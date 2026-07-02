# Session Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlNlc3Npb25Db25maWd1cmF0aW9u

Contains session configuration information.


# Class Name

`SessionConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ExecutionRole` | `String` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` | String getExecutionRole() | setExecutionRole(String executionRole) |
| `WorkingDirectory` | `String` | Optional | - | String getWorkingDirectory() | setWorkingDirectory(String workingDirectory) |
| `IdleTimeoutSeconds` | `Integer` | Optional | - | Integer getIdleTimeoutSeconds() | setIdleTimeoutSeconds(Integer idleTimeoutSeconds) |
| `EncryptionConfiguration` | [`EncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/encryption-configuration.md) | Optional | If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information. | EncryptionConfiguration getEncryptionConfiguration() | setEncryptionConfiguration(EncryptionConfiguration encryptionConfiguration) |


# Example

```java
import com.amazonaws.useast1.athena.models.EncryptionConfiguration;
import com.amazonaws.useast1.athena.models.EncryptionOption1Enum;
import com.amazonaws.useast1.athena.models.SessionConfiguration;

SessionConfiguration sessionConfiguration = new SessionConfiguration.Builder()
    .executionRole("ExecutionRole2")
    .workingDirectory("WorkingDirectory6")
    .idleTimeoutSeconds(188)
    .encryptionConfiguration(new EncryptionConfiguration.Builder(
        EncryptionOption1Enum.SSE_S3
    )
    .kmsKey("KmsKey6")
    .build())
    .build();
```



