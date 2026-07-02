# Get Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFPdXRwdXQ


# Class Name

`GetTableMetadataOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TableMetadata` | [`TableMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/table-metadata-2.md) | Optional | - | TableMetadata2 getTableMetadata() | setTableMetadata(TableMetadata2 tableMetadata) |


# Example

```java
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.Column;
import com.amazonaws.useast1.athena.models.GetTableMetadataOutput;
import com.amazonaws.useast1.athena.models.TableMetadata2;
import java.util.Arrays;

GetTableMetadataOutput getTableMetadataOutput = new GetTableMetadataOutput.Builder()
    .tableMetadata(new TableMetadata2.Builder(
        "Name6"
    )
    .createTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .lastAccessTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .tableType("TableType0")
    .columns(Arrays.asList(
            new Column.Builder(
                "Name0"
            )
            .type("Type0")
            .comment("Comment4")
            .build(),
            new Column.Builder(
                "Name0"
            )
            .type("Type0")
            .comment("Comment4")
            .build(),
            new Column.Builder(
                "Name0"
            )
            .type("Type0")
            .comment("Comment4")
            .build()
        ))
    .partitionKeys(Arrays.asList(
            new Column.Builder(
                "Name6"
            )
            .type("Type6")
            .comment("Comment0")
            .build()
        ))
    .build())
    .build();
```



