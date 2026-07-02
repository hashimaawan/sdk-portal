# Get Query Results Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldFF1ZXJ5UmVzdWx0c091dHB1dA

*This model accepts additional fields of type Object.*


# Class Name

`GetQueryResultsOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `UpdateCount` | `Integer` | Optional | - | Integer getUpdateCount() | setUpdateCount(Integer updateCount) |
| `ResultSet` | [`ResultSet2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/result-set-2.md) | Optional | - | ResultSet2 getResultSet() | setResultSet(ResultSet2 resultSet) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ColumnInfo;
import com.amazonaws.useast1.athena.models.Datum;
import com.amazonaws.useast1.athena.models.GetQueryResultsOutput;
import com.amazonaws.useast1.athena.models.ResultSet2;
import com.amazonaws.useast1.athena.models.ResultSetMetadata2;
import com.amazonaws.useast1.athena.models.Row;
import java.io.IOException;
import java.util.Arrays;

GetQueryResultsOutput getQueryResultsOutput = new GetQueryResultsOutput.Builder()
    .updateCount(60)
    .resultSet(new ResultSet2.Builder()
        .rows(Arrays.asList(
            new Row.Builder()
                .data(Arrays.asList(
                    new Datum.Builder()
                        .varCharValue("VarCharValue8")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new Datum.Builder()
                        .varCharValue("VarCharValue8")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new Row.Builder()
                .data(Arrays.asList(
                    new Datum.Builder()
                        .varCharValue("VarCharValue8")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new Datum.Builder()
                        .varCharValue("VarCharValue8")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
        .resultSetMetadata(new ResultSetMetadata2.Builder()
            .columnInfo(Arrays.asList(
                new ColumnInfo.Builder(
                    "Name6",
                    "Type6"
                )
                .catalogName("CatalogName0")
                .schemaName("SchemaName0")
                .tableName("TableName2")
                .label("Label4")
                .precision(48)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .nextToken("NextToken0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



