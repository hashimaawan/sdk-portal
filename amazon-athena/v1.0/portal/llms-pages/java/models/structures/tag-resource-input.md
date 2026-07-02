# Tag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlRhZ1Jlc291cmNlSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`TagResourceInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ResourceArn` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` | String getResourceArn() | setResourceArn(String resourceArn) |
| `Tags` | [`List<Tag>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/tag.md) | Required | - | List<Tag> getTags() | setTags(List<Tag> tags) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.Tag;
import com.amazonaws.useast1.athena.models.TagResourceInput;
import java.io.IOException;
import java.util.Arrays;

TagResourceInput tagResourceInput = new TagResourceInput.Builder(
    "ResourceARN6",
    Arrays.asList(
        new Tag.Builder()
            .key("Key0")
            .value("Value6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



