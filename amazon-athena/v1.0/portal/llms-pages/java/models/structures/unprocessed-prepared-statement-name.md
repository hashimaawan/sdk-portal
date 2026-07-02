# Unprocessed Prepared Statement Name

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkUHJlcGFyZWRTdGF0ZW1lbnROYW1l

The name of a prepared statement that could not be returned.

*This model accepts additional fields of type Object.*


# Class Name

`UnprocessedPreparedStatementName`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StatementName` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` | String getStatementName() | setStatementName(String statementName) |
| `ErrorCode` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getErrorCode() | setErrorCode(String errorCode) |
| `ErrorMessage` | `String` | Optional | - | String getErrorMessage() | setErrorMessage(String errorMessage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.UnprocessedPreparedStatementName;
import java.io.IOException;

UnprocessedPreparedStatementName unprocessedPreparedStatementName = new UnprocessedPreparedStatementName.Builder()
    .statementName("StatementName8")
    .errorCode("ErrorCode6")
    .errorMessage("ErrorMessage6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



