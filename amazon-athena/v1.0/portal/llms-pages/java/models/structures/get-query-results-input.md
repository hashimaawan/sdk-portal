# Get Query Results Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldFF1ZXJ5UmVzdWx0c0lucHV0


# Class Name

`GetQueryResultsInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `QueryExecutionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | String getQueryExecutionId() | setQueryExecutionId(String queryExecutionId) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 1000` | Integer getMaxResults() | setMaxResults(Integer maxResults) |


# Example

```java
import com.amazonaws.useast1.athena.models.GetQueryResultsInput;

GetQueryResultsInput getQueryResultsInput = new GetQueryResultsInput.Builder(
    "QueryExecutionId6"
)
.nextToken("NextToken2")
.maxResults(42)
.build();
```



