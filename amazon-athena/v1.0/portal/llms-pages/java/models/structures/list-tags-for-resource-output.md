# List Tags for Resource Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RUYWdzRm9yUmVzb3VyY2VPdXRwdXQ


# Class Name

`ListTagsForResourceOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Tags` | [`List<Tag>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/tag.md) | Optional | - | List<Tag> getTags() | setTags(List<Tag> tags) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |


# Example

```java
import com.amazonaws.useast1.athena.models.ListTagsForResourceOutput;
import com.amazonaws.useast1.athena.models.Tag;
import java.util.Arrays;

ListTagsForResourceOutput listTagsForResourceOutput = new ListTagsForResourceOutput.Builder()
    .tags(Arrays.asList(
        new Tag.Builder()
            .key("Key0")
            .value("Value6")
            .build(),
        new Tag.Builder()
            .key("Key0")
            .value("Value6")
            .build(),
        new Tag.Builder()
            .key("Key0")
            .value("Value6")
            .build()
    ))
    .nextToken("NextToken4")
    .build();
```



