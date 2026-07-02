# Untag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlVudGFnUmVzb3VyY2VJbnB1dA


# Class Name

`UntagResourceInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ResourceARN` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` | String getResourceARN() | setResourceARN(String resourceARN) |
| `TagKeys` | `List<String>` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | List<String> getTagKeys() | setTagKeys(List<String> tagKeys) |


# Example

```java
import com.amazonaws.useast1.athena.models.UntagResourceInput;
import java.util.Arrays;

UntagResourceInput untagResourceInput = new UntagResourceInput.Builder(
    "ResourceARN6",
    Arrays.asList(
        "TagKeys1",
        "TagKeys2",
        "TagKeys3"
    )
)
.build();
```



