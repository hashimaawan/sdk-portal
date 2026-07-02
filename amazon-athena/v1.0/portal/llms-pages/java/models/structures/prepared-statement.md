# Prepared Statement

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlByZXBhcmVkU3RhdGVtZW50

A prepared SQL statement for use with Athena.

*This model accepts additional fields of type Object.*


# Class Name

`PreparedStatement`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StatementName` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` | String getStatementName() | setStatementName(String statementName) |
| `QueryStatement` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` | String getQueryStatement() | setQueryStatement(String queryStatement) |
| `WorkGroupName` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroupName() | setWorkGroupName(String workGroupName) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `LastModifiedTime` | `LocalDateTime` | Optional | - | LocalDateTime getLastModifiedTime() | setLastModifiedTime(LocalDateTime lastModifiedTime) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.PreparedStatement;
import java.io.IOException;

PreparedStatement preparedStatement = new PreparedStatement.Builder()
    .statementName("StatementName8")
    .queryStatement("QueryStatement2")
    .workGroupName("WorkGroupName2")
    .description("Description4")
    .lastModifiedTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



