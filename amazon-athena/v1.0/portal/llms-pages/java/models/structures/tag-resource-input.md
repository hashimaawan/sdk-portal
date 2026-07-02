# Tag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlRhZ1Jlc291cmNlSW5wdXQ


# Class Name

`TagResourceInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ResourceARN` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` | String getResourceARN() | setResourceARN(String resourceARN) |
| `Tags` | [`List<Tag>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/tag.md) | Required | - | List<Tag> getTags() | setTags(List<Tag> tags) |


# Example

```java
import com.amazonaws.useast1.athena.models.Tag;
import com.amazonaws.useast1.athena.models.TagResourceInput;
import java.util.Arrays;

TagResourceInput tagResourceInput = new TagResourceInput.Builder(
    "ResourceARN6",
    Arrays.asList(
        new Tag.Builder()
            .key("Key0")
            .value("Value6")
            .build()
    )
)
.build();
```



