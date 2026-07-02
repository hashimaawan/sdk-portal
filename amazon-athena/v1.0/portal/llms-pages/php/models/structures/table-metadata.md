# Table Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlRhYmxlTWV0YWRhdGE

Contains metadata for a table.

*This model accepts additional fields of type array.*


# Class Name

`TableMetadata`


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
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\TableMetadataBuilder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\Builders\ColumnBuilder;
use AmazonAthenaLib\ApiHelper;

$tableMetadata = TableMetadataBuilder::init(
    'Name0'
)
    ->createTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->lastAccessTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->tableType('TableType4')
    ->columns(
        [
            ColumnBuilder::init(
                'Name0'
            )
                ->type('Type0')
                ->comment('Comment4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
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
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ColumnBuilder::init(
                'Name6'
            )
                ->type('Type6')
                ->comment('Comment0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ColumnBuilder::init(
                'Name6'
            )
                ->type('Type6')
                ->comment('Comment0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



