# List Prepared Statements Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RQcmVwYXJlZFN0YXRlbWVudHNPdXRwdXQ


# Class Name

`ListPreparedStatementsOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PreparedStatements` | [`List<PreparedStatementSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/prepared-statement-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `50` | List<PreparedStatementSummary> getPreparedStatements() | setPreparedStatements(List<PreparedStatementSummary> preparedStatements) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |


# Example

```java
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.ListPreparedStatementsOutput;
import com.amazonaws.useast1.athena.models.PreparedStatementSummary;
import java.util.Arrays;

ListPreparedStatementsOutput listPreparedStatementsOutput = new ListPreparedStatementsOutput.Builder()
    .preparedStatements(Arrays.asList(
        new PreparedStatementSummary.Builder()
            .statementName("StatementName2")
            .lastModifiedTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .build(),
        new PreparedStatementSummary.Builder()
            .statementName("StatementName2")
            .lastModifiedTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .build()
    ))
    .nextToken("NextToken2")
    .build();
```



