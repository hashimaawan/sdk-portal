# Result Set Metadata 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRhMg


# Class Name

`ResultSetMetadata2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ColumnInfo` | [`List<ColumnInfo>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/column-info.md) | Optional | - | List<ColumnInfo> getColumnInfo() | setColumnInfo(List<ColumnInfo> columnInfo) |


# Example

```java
import com.amazonaws.useast1.athena.models.ColumnInfo;
import com.amazonaws.useast1.athena.models.ResultSetMetadata2;
import java.util.Arrays;

ResultSetMetadata2 resultSetMetadata2 = new ResultSetMetadata2.Builder()
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



