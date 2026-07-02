# Get Query Results Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldFF1ZXJ5UmVzdWx0c0lucHV0

*This model accepts additional fields of type Object.*


# Class Name

`GetQueryResultsInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `QueryExecutionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | String getQueryExecutionId() | setQueryExecutionId(String queryExecutionId) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 1000` | Integer getMaxResults() | setMaxResults(Integer maxResults) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.GetQueryResultsInput;
import java.io.IOException;

GetQueryResultsInput getQueryResultsInput = new GetQueryResultsInput.Builder(
    "QueryExecutionId6"
)
.nextToken("NextToken2")
.maxResults(42)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



