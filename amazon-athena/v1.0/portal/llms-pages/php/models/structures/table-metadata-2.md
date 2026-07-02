# Table Metadata 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlRhYmxlTWV0YWRhdGEy


# Class Name

`TableMetadata2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getName(): string | setName(string name): void |
| `createTime` | `?DateTime` | Optional | - | getCreateTime(): ?\DateTime | setCreateTime(?\DateTime createTime): void |
| `lastAccessTime` | `?DateTime` | Optional | - | getLastAccessTime(): ?\DateTime | setLastAccessTime(?\DateTime lastAccessTime): void |
| `tableType` | `?string` | Optional | **Constraints**: *Maximum Length*: `255` | getTableType(): ?string | setTableType(?string tableType): void |
| `columns` | [`?(Column[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/column.md) | Optional | - | getColumns(): ?array | setColumns(?array columns): void |
| `partitionKeys` | [`?(Column[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/column.md) | Optional | - | getPartitionKeys(): ?array | setPartitionKeys(?array partitionKeys): void |
| `parameters` | [`?Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/parameters.md) | Optional | - | getParameters(): ?Parameters | setParameters(?Parameters parameters): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\TableMetadata2Builder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\Builders\ColumnBuilder;

$tableMetadata2 = TableMetadata2Builder::init(
    'Name8'
)
    ->createTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->lastAccessTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->tableType('TableType6')
    ->columns(
        [
            ColumnBuilder::init(
                'Name0'
            )
                ->type('Type0')
                ->comment('Comment4')
                ->build(),
            ColumnBuilder::init(
                'Name0'
            )
                ->type('Type0')
                ->comment('Comment4')
                ->build()
        ]
    )
    ->partitionKeys(
        [
            ColumnBuilder::init(
                'Name6'
            )
                ->type('Type6')
                ->comment('Comment0')
                ->build(),
            ColumnBuilder::init(
                'Name6'
            )
                ->type('Type6')
                ->comment('Comment0')
                ->build()
        ]
    )
    ->build();
```



