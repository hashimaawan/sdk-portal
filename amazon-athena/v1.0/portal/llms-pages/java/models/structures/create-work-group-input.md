# Create Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZVdvcmtHcm91cElucHV0

*This model accepts additional fields of type Object.*


# Class Name

`CreateWorkGroupInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getName() | setName(String name) |
| `Configuration` | [`Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/configuration.md) | Optional | - | Configuration getConfiguration() | setConfiguration(Configuration configuration) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `Tags` | [`List<Tag>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/tag.md) | Optional | - | List<Tag> getTags() | setTags(List<Tag> tags) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.AclConfiguration1;
import com.amazonaws.useast1.athena.models.Configuration;
import com.amazonaws.useast1.athena.models.CreateWorkGroupInput;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1;
import com.amazonaws.useast1.athena.models.ResultConfiguration1;
import com.amazonaws.useast1.athena.models.S3AclOption1;
import com.amazonaws.useast1.athena.models.Tag;
import java.io.IOException;
import java.util.Arrays;

CreateWorkGroupInput createWorkGroupInput = new CreateWorkGroupInput.Builder(
    "Name6"
)
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
.description("Description0")
.tags(Arrays.asList(
        new Tag.Builder()
            .key("Key0")
            .value("Value6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Tag.Builder()
            .key("Key0")
            .value("Value6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



