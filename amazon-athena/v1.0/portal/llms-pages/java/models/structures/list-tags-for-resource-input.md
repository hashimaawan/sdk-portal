# List Tags for Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RUYWdzRm9yUmVzb3VyY2VJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`ListTagsForResourceInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ResourceArn` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` | String getResourceArn() | setResourceArn(String resourceArn) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 75` | Integer getMaxResults() | setMaxResults(Integer maxResults) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ListTagsForResourceInput;
import java.io.IOException;

ListTagsForResourceInput listTagsForResourceInput = new ListTagsForResourceInput.Builder(
    "ResourceARN0"
)
.nextToken("NextToken0")
.maxResults(76)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



