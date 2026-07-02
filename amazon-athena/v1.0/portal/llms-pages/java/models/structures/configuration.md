# Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNvbmZpZ3VyYXRpb24

*This model accepts additional fields of type Object.*


# Class Name

`Configuration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ResultConfiguration` | [`ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/result-configuration-1.md) | Optional | - | ResultConfiguration1 getResultConfiguration() | setResultConfiguration(ResultConfiguration1 resultConfiguration) |
| `EnforceWorkGroupConfiguration` | `Boolean` | Optional | - | Boolean getEnforceWorkGroupConfiguration() | setEnforceWorkGroupConfiguration(Boolean enforceWorkGroupConfiguration) |
| `PublishCloudWatchMetricsEnabled` | `Boolean` | Optional | - | Boolean getPublishCloudWatchMetricsEnabled() | setPublishCloudWatchMetricsEnabled(Boolean publishCloudWatchMetricsEnabled) |
| `BytesScannedCutoffPerQuery` | `Integer` | Optional | **Constraints**: `>= 10000000` | Integer getBytesScannedCutoffPerQuery() | setBytesScannedCutoffPerQuery(Integer bytesScannedCutoffPerQuery) |
| `RequesterPaysEnabled` | `Boolean` | Optional | - | Boolean getRequesterPaysEnabled() | setRequesterPaysEnabled(Boolean requesterPaysEnabled) |
| `EngineVersion` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/engine-version-1.md) | Optional | - | EngineVersion1 getEngineVersion() | setEngineVersion(EngineVersion1 engineVersion) |
| `AdditionalConfiguration` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getAdditionalConfiguration() | setAdditionalConfiguration(String additionalConfiguration) |
| `ExecutionRole` | `String` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` | String getExecutionRole() | setExecutionRole(String executionRole) |
| `CustomerContentEncryptionConfiguration` | [`CustomerContentEncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/customer-content-encryption-configuration-2.md) | Optional | - | CustomerContentEncryptionConfiguration2 getCustomerContentEncryptionConfiguration() | setCustomerContentEncryptionConfiguration(CustomerContentEncryptionConfiguration2 customerContentEncryptionConfiguration) |
| `EnableMinimumEncryptionConfiguration` | `Boolean` | Optional | - | Boolean getEnableMinimumEncryptionConfiguration() | setEnableMinimumEncryptionConfiguration(Boolean enableMinimumEncryptionConfiguration) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.AclConfiguration1;
import com.amazonaws.useast1.athena.models.Configuration;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1;
import com.amazonaws.useast1.athena.models.ResultConfiguration1;
import com.amazonaws.useast1.athena.models.S3AclOption1;
import java.io.IOException;

Configuration configuration = new Configuration.Builder()
    .resultConfiguration(new ResultConfiguration1.Builder()
        .outputLocation("OutputLocation0")
        .encryptionConfiguration(new EncryptionConfiguration2.Builder(
            EncryptionOption1.SSE_S3
        )
        .kmsKey("KmsKey6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
        .expectedBucketOwner("ExpectedBucketOwner0")
        .aclConfiguration(new AclConfiguration1.Builder(
            S3AclOption1.BUCKET_OWNER_FULL_CONTROL
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .enforceWorkGroupConfiguration(false)
    .publishCloudWatchMetricsEnabled(false)
    .bytesScannedCutoffPerQuery(10000000)
    .requesterPaysEnabled(false)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



