# Update Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlVwZGF0ZVdvcmtHcm91cElucHV0

*This model accepts additional fields of type Object.*


# Class Name

`UpdateWorkGroupInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `WorkGroup` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `ConfigurationUpdates` | [`ConfigurationUpdates`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/configuration-updates.md) | Optional | - | ConfigurationUpdates getConfigurationUpdates() | setConfigurationUpdates(ConfigurationUpdates configurationUpdates) |
| `State` | [`WorkGroupState2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/work-group-state-2.md) | Optional | - | WorkGroupState2 getState() | setState(WorkGroupState2 state) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ConfigurationUpdates;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1;
import com.amazonaws.useast1.athena.models.ResultConfigurationUpdates2;
import com.amazonaws.useast1.athena.models.UpdateWorkGroupInput;
import com.amazonaws.useast1.athena.models.WorkGroupState2;
import java.io.IOException;

UpdateWorkGroupInput updateWorkGroupInput = new UpdateWorkGroupInput.Builder(
    "WorkGroup0"
)
.description("Description8")
.configurationUpdates(new ConfigurationUpdates.Builder()
        .enforceWorkGroupConfiguration(false)
        .resultConfigurationUpdates(new ResultConfigurationUpdates2.Builder()
            .outputLocation("OutputLocation0")
            .removeOutputLocation(false)
            .encryptionConfiguration(new EncryptionConfiguration2.Builder(
                EncryptionOption1.SSE_S3
            )
            .kmsKey("KmsKey6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
            .removeEncryptionConfiguration(false)
            .expectedBucketOwner("ExpectedBucketOwner0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .publishCloudWatchMetricsEnabled(false)
        .bytesScannedCutoffPerQuery(10000000)
        .removeBytesScannedCutoffPerQuery(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.state(WorkGroupState2.ENABLED)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



