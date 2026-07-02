# Result Set 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlJlc3VsdFNldDI


# Class Name

`ResultSet2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Rows` | [`List<Row>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/row.md) | Optional | - | List<Row> getRows() | setRows(List<Row> rows) |
| `ResultSetMetadata` | [`ResultSetMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/result-set-metadata-2.md) | Optional | - | ResultSetMetadata2 getResultSetMetadata() | setResultSetMetadata(ResultSetMetadata2 resultSetMetadata) |


# Example

```java
import com.amazonaws.useast1.athena.models.ColumnInfo;
import com.amazonaws.useast1.athena.models.Datum;
import com.amazonaws.useast1.athena.models.ResultSet2;
import com.amazonaws.useast1.athena.models.ResultSetMetadata2;
import com.amazonaws.useast1.athena.models.Row;
import java.util.Arrays;

ResultSet2 resultSet2 = new ResultSet2.Builder()
    .rows(Arrays.asList(
        new Row.Builder()
            .data(Arrays.asList(
                new Datum.Builder()
                    .varCharValue("VarCharValue8")
                    .build(),
                new Datum.Builder()
                    .varCharValue("VarCharValue8")
                    .build()
            ))
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
            .build()
        ))
        .build())
    .build();
```



