# Untag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlVudGFnUmVzb3VyY2VJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`UntagResourceInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ResourceArn` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` | String getResourceArn() | setResourceArn(String resourceArn) |
| `TagKeys` | `List<String>` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | List<String> getTagKeys() | setTagKeys(List<String> tagKeys) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.UntagResourceInput;
import java.io.IOException;
import java.util.Arrays;

UntagResourceInput untagResourceInput = new UntagResourceInput.Builder(
    "ResourceARN6",
    Arrays.asList(
        "TagKeys1",
        "TagKeys2",
        "TagKeys3"
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



