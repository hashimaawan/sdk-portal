# Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldFByZXBhcmVkU3RhdGVtZW50T3V0cHV0

*This model accepts additional fields of type Object.*


# Class Name

`GetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PreparedStatement` | [`PreparedStatement1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/prepared-statement-1.md) | Optional | - | PreparedStatement1 getPreparedStatement() | setPreparedStatement(PreparedStatement1 preparedStatement) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.GetPreparedStatementOutput;
import com.amazonaws.useast1.athena.models.PreparedStatement1;
import java.io.IOException;

GetPreparedStatementOutput getPreparedStatementOutput = new GetPreparedStatementOutput.Builder()
    .preparedStatement(new PreparedStatement1.Builder()
        .statementName("StatementName4")
        .queryStatement("QueryStatement8")
        .workGroupName("WorkGroupName8")
        .description("Description0")
        .lastModifiedTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



