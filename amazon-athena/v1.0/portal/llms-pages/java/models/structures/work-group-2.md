# Work Group 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRldvcmtHcm91cDI

*This model accepts additional fields of type Object.*


# Class Name

`WorkGroup2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getName() | setName(String name) |
| `State` | [`WorkGroupState3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/work-group-state-3.md) | Optional | - | WorkGroupState3 getState() | setState(WorkGroupState3 state) |
| `Configuration` | [`Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/configuration.md) | Optional | - | Configuration getConfiguration() | setConfiguration(Configuration configuration) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `CreationTime` | `LocalDateTime` | Optional | - | LocalDateTime getCreationTime() | setCreationTime(LocalDateTime creationTime) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.AclConfiguration1;
import com.amazonaws.useast1.athena.models.Configuration;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1;
import com.amazonaws.useast1.athena.models.ResultConfiguration1;
import com.amazonaws.useast1.athena.models.S3AclOption1;
import com.amazonaws.useast1.athena.models.WorkGroup2;
import com.amazonaws.useast1.athena.models.WorkGroupState3;
import java.io.IOException;

WorkGroup2 workGroup2 = new WorkGroup2.Builder(
    "Name0"
)
.state(WorkGroupState3.ENABLED)
.configuration(new Configuration.Builder()
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
        .build())
.description("Description6")
.creationTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



