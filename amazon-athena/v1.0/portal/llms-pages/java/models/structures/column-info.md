# Column Info

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNvbHVtbkluZm8

Information about the columns in a query execution result.


# Class Name

`ColumnInfo`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CatalogName` | `String` | Optional | - | String getCatalogName() | setCatalogName(String catalogName) |
| `SchemaName` | `String` | Optional | - | String getSchemaName() | setSchemaName(String schemaName) |
| `TableName` | `String` | Optional | - | String getTableName() | setTableName(String tableName) |
| `Name` | `String` | Required | - | String getName() | setName(String name) |
| `Label` | `String` | Optional | - | String getLabel() | setLabel(String label) |
| `Type` | `String` | Required | - | String getType() | setType(String type) |
| `Precision` | `Integer` | Optional | - | Integer getPrecision() | setPrecision(Integer precision) |
| `Scale` | `Integer` | Optional | - | Integer getScale() | setScale(Integer scale) |
| `Nullable` | [`ColumnNullable2Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/column-nullable-2.md) | Optional | - | ColumnNullable2Enum getNullable() | setNullable(ColumnNullable2Enum nullable) |
| `CaseSensitive` | `Boolean` | Optional | - | Boolean getCaseSensitive() | setCaseSensitive(Boolean caseSensitive) |


# Example

```java
import com.amazonaws.useast1.athena.models.ColumnInfo;

ColumnInfo columnInfo = new ColumnInfo.Builder(
    "Name8",
    "Type8"
)
.catalogName("CatalogName2")
.schemaName("SchemaName2")
.tableName("TableName4")
.label("Label6")
.precision(196)
.build();
```



