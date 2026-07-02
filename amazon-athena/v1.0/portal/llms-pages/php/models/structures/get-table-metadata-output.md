# Get Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFPdXRwdXQ


# Class Name

`GetTableMetadataOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `tableMetadata` | [`?TableMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/table-metadata-2.md) | Optional | - | getTableMetadata(): ?TableMetadata2 | setTableMetadata(?TableMetadata2 tableMetadata): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetTableMetadataOutputBuilder;
use AmazonAthenaLib\Models\Builders\TableMetadata2Builder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\Builders\ColumnBuilder;

$getTableMetadataOutput = GetTableMetadataOutputBuilder::init()
    ->tableMetadata(
        TableMetadata2Builder::init(
            'Name6'
        )
            ->createTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->lastAccessTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->tableType('TableType0')
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
                        ->build()
                ]
            )
            ->build()
    )
    ->build();
```



