# Unprocessed Query Execution Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkUXVlcnlFeGVjdXRpb25JZA

Describes a query execution that failed to process.

*This model accepts additional fields of type Object.*


# Class Name

`UnprocessedQueryExecutionId`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `QueryExecutionId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | String getQueryExecutionId() | setQueryExecutionId(String queryExecutionId) |
| `ErrorCode` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getErrorCode() | setErrorCode(String errorCode) |
| `ErrorMessage` | `String` | Optional | - | String getErrorMessage() | setErrorMessage(String errorMessage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.UnprocessedQueryExecutionId;
import java.io.IOException;

UnprocessedQueryExecutionId unprocessedQueryExecutionId = new UnprocessedQueryExecutionId.Builder()
    .queryExecutionId("QueryExecutionId6")
    .errorCode("ErrorCode2")
    .errorMessage("ErrorMessage8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



