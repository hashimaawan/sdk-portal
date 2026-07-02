# List Engine Versions Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc0lucHV0

*This model accepts additional fields of type Object.*


# Class Name

`ListEngineVersionsInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 10` | Integer getMaxResults() | setMaxResults(Integer maxResults) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ListEngineVersionsInput;
import java.io.IOException;

ListEngineVersionsInput listEngineVersionsInput = new ListEngineVersionsInput.Builder()
    .nextToken("NextToken6")
    .maxResults(10)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



