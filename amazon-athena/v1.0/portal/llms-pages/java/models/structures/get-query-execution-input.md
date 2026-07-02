# Get Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldFF1ZXJ5RXhlY3V0aW9uSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`GetQueryExecutionInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `QueryExecutionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | String getQueryExecutionId() | setQueryExecutionId(String queryExecutionId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.GetQueryExecutionInput;
import java.io.IOException;

GetQueryExecutionInput getQueryExecutionInput = new GetQueryExecutionInput.Builder(
    "QueryExecutionId8"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



