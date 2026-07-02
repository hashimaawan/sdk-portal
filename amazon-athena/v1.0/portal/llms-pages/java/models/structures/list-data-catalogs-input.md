# List Data Catalogs Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`ListDataCatalogsInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 2`, `<= 50` | Integer getMaxResults() | setMaxResults(Integer maxResults) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ListDataCatalogsInput;
import java.io.IOException;

ListDataCatalogsInput listDataCatalogsInput = new ListDataCatalogsInput.Builder()
    .nextToken("NextToken8")
    .maxResults(50)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



