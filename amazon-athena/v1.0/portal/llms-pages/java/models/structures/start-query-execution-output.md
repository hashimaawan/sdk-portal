# Start Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXJ0UXVlcnlFeGVjdXRpb25PdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`StartQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `QueryExecutionId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | String getQueryExecutionId() | setQueryExecutionId(String queryExecutionId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.StartQueryExecutionOutput;
import java.io.IOException;

StartQueryExecutionOutput startQueryExecutionOutput = new StartQueryExecutionOutput.Builder()
    .queryExecutionId("QueryExecutionId0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



