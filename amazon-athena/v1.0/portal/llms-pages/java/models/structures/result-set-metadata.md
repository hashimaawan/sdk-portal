# Result Set Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRh

The metadata that describes the column structure and data types of a table of query results. To return a <code>ResultSetMetadata</code> object, use <a>GetQueryResults</a>.


# Class Name

`ResultSetMetadata`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ColumnInfo` | [`List<ColumnInfo>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/column-info.md) | Optional | - | List<ColumnInfo> getColumnInfo() | setColumnInfo(List<ColumnInfo> columnInfo) |


# Example

```java
import com.amazonaws.useast1.athena.models.ColumnInfo;
import com.amazonaws.useast1.athena.models.ResultSetMetadata;
import java.util.Arrays;

ResultSetMetadata resultSetMetadata = new ResultSetMetadata.Builder()
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
        .build(),
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
    .build();
```



