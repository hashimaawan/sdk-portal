# Prepared Statement 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlByZXBhcmVkU3RhdGVtZW50MQ


# Class Name

`PreparedStatement1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StatementName` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` | String getStatementName() | setStatementName(String statementName) |
| `QueryStatement` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` | String getQueryStatement() | setQueryStatement(String queryStatement) |
| `WorkGroupName` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroupName() | setWorkGroupName(String workGroupName) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `LastModifiedTime` | `LocalDateTime` | Optional | - | LocalDateTime getLastModifiedTime() | setLastModifiedTime(LocalDateTime lastModifiedTime) |


# Example

```java
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.PreparedStatement1;

PreparedStatement1 preparedStatement1 = new PreparedStatement1.Builder()
    .statementName("StatementName6")
    .queryStatement("QueryStatement0")
    .workGroupName("WorkGroupName0")
    .description("Description8")
    .lastModifiedTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .build();
```



