# Batch Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnRPdXRwdXQ


# Class Name

`BatchGetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PreparedStatements` | [`List<PreparedStatement>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/prepared-statement.md) | Optional | - | List<PreparedStatement> getPreparedStatements() | setPreparedStatements(List<PreparedStatement> preparedStatements) |
| `UnprocessedPreparedStatementNames` | [`List<UnprocessedPreparedStatementName>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/unprocessed-prepared-statement-name.md) | Optional | - | List<UnprocessedPreparedStatementName> getUnprocessedPreparedStatementNames() | setUnprocessedPreparedStatementNames(List<UnprocessedPreparedStatementName> unprocessedPreparedStatementNames) |


# Example

```java
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.BatchGetPreparedStatementOutput;
import com.amazonaws.useast1.athena.models.PreparedStatement;
import com.amazonaws.useast1.athena.models.UnprocessedPreparedStatementName;
import java.util.Arrays;

BatchGetPreparedStatementOutput batchGetPreparedStatementOutput = new BatchGetPreparedStatementOutput.Builder()
    .preparedStatements(Arrays.asList(
        new PreparedStatement.Builder()
            .statementName("StatementName2")
            .queryStatement("QueryStatement6")
            .workGroupName("WorkGroupName6")
            .description("Description2")
            .lastModifiedTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .build(),
        new PreparedStatement.Builder()
            .statementName("StatementName2")
            .queryStatement("QueryStatement6")
            .workGroupName("WorkGroupName6")
            .description("Description2")
            .lastModifiedTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .build()
    ))
    .unprocessedPreparedStatementNames(Arrays.asList(
        new UnprocessedPreparedStatementName.Builder()
            .statementName("StatementName0")
            .errorCode("ErrorCode2")
            .errorMessage("ErrorMessage8")
            .build(),
        new UnprocessedPreparedStatementName.Builder()
            .statementName("StatementName0")
            .errorCode("ErrorCode2")
            .errorMessage("ErrorMessage8")
            .build(),
        new UnprocessedPreparedStatementName.Builder()
            .statementName("StatementName0")
            .errorCode("ErrorCode2")
            .errorMessage("ErrorMessage8")
            .build()
    ))
    .build();
```



