# List Query Executions Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RRdWVyeUV4ZWN1dGlvbnNPdXRwdXQ


# Class Name

`ListQueryExecutionsOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `QueryExecutionIds` | `List<String>` | Optional | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | List<String> getQueryExecutionIds() | setQueryExecutionIds(List<String> queryExecutionIds) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |


# Example

```java
import com.amazonaws.useast1.athena.models.ListQueryExecutionsOutput;
import java.util.Arrays;

ListQueryExecutionsOutput listQueryExecutionsOutput = new ListQueryExecutionsOutput.Builder()
    .queryExecutionIds(Arrays.asList(
        "QueryExecutionIds9"
    ))
    .nextToken("NextToken2")
    .build();
```



