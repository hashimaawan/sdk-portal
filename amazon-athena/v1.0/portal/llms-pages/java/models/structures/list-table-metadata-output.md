# List Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhT3V0cHV0

*This model accepts additional fields of type Object.*


# Class Name

`ListTableMetadataOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TableMetadataList` | [`List<TableMetadata>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/table-metadata.md) | Optional | - | List<TableMetadata> getTableMetadataList() | setTableMetadataList(List<TableMetadata> tableMetadataList) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.Column;
import com.amazonaws.useast1.athena.models.ListTableMetadataOutput;
import com.amazonaws.useast1.athena.models.TableMetadata;
import java.io.IOException;
import java.util.Arrays;

ListTableMetadataOutput listTableMetadataOutput = new ListTableMetadataOutput.Builder()
    .tableMetadataList(Arrays.asList(
        new TableMetadata.Builder(
            "Name2"
        )
        .createTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .lastAccessTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .tableType("TableType2")
        .columns(Arrays.asList(
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
        .build(),
        new TableMetadata.Builder(
            "Name2"
        )
        .createTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .lastAccessTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .tableType("TableType2")
        .columns(Arrays.asList(
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
        .build()
    ))
    .nextToken("NextToken0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



