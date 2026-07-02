# Batch Get Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25JbnB1dA

Contains an array of query execution IDs.

*This model accepts additional fields of type Object.*


# Class Name

`BatchGetQueryExecutionInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `QueryExecutionIds` | `List<String>` | Required | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | List<String> getQueryExecutionIds() | setQueryExecutionIds(List<String> queryExecutionIds) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.BatchGetQueryExecutionInput;
import java.io.IOException;
import java.util.Arrays;

BatchGetQueryExecutionInput batchGetQueryExecutionInput = new BatchGetQueryExecutionInput.Builder(
    Arrays.asList(
        "QueryExecutionIds7",
        "QueryExecutionIds8",
        "QueryExecutionIds9"
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



