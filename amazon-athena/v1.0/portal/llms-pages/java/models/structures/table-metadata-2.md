# Table Metadata 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlRhYmxlTWV0YWRhdGEy

*This model accepts additional fields of type Object.*


# Class Name

`TableMetadata2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getName() | setName(String name) |
| `CreateTime` | `LocalDateTime` | Optional | - | LocalDateTime getCreateTime() | setCreateTime(LocalDateTime createTime) |
| `LastAccessTime` | `LocalDateTime` | Optional | - | LocalDateTime getLastAccessTime() | setLastAccessTime(LocalDateTime lastAccessTime) |
| `TableType` | `String` | Optional | **Constraints**: *Maximum Length*: `255` | String getTableType() | setTableType(String tableType) |
| `Columns` | [`List<Column>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/column.md) | Optional | - | List<Column> getColumns() | setColumns(List<Column> columns) |
| `PartitionKeys` | [`List<Column>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/column.md) | Optional | - | List<Column> getPartitionKeys() | setPartitionKeys(List<Column> partitionKeys) |
| `Parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/parameters.md) | Optional | - | Parameters getParameters() | setParameters(Parameters parameters) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.Column;
import com.amazonaws.useast1.athena.models.TableMetadata2;
import java.io.IOException;
import java.util.Arrays;

TableMetadata2 tableMetadata2 = new TableMetadata2.Builder(
    "Name8"
)
.createTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
.lastAccessTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
.tableType("TableType6")
.columns(Arrays.asList(
        new Column.Builder(
            "Name0"
        )
        .type("Type0")
        .comment("Comment4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Column.Builder(
            "Name0"
        )
        .type("Type0")
        .comment("Comment4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.partitionKeys(Arrays.asList(
        new Column.Builder(
            "Name6"
        )
        .type("Type6")
        .comment("Comment0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Column.Builder(
            "Name6"
        )
        .type("Type6")
        .comment("Comment0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



