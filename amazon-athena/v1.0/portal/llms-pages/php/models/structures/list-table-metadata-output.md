# List Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhT3V0cHV0


# Class Name

`ListTableMetadataOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `tableMetadataList` | [`?(TableMetadata[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/table-metadata.md) | Optional | - | getTableMetadataList(): ?array | setTableMetadataList(?array tableMetadataList): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListTableMetadataOutputBuilder;
use AmazonAthenaLib\Models\Builders\TableMetadataBuilder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\Builders\ColumnBuilder;

$listTableMetadataOutput = ListTableMetadataOutputBuilder::init()
    ->tableMetadataList(
        [
            TableMetadataBuilder::init(
                'Name2'
            )
                ->createTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->lastAccessTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->tableType('TableType2')
                ->columns(
                    [
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
                            ->build(),
                        ColumnBuilder::init(
                            'Name6'
                        )
                            ->type('Type6')
                            ->comment('Comment0')
                            ->build()
                    ]
                )
                ->build(),
            TableMetadataBuilder::init(
                'Name2'
            )
                ->createTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->lastAccessTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->tableType('TableType2')
                ->columns(
                    [
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
                            ->build(),
                        ColumnBuilder::init(
                            'Name6'
                        )
                            ->type('Type6')
                            ->comment('Comment0')
                            ->build()
                    ]
                )
                ->build()
        ]
    )
    ->nextToken('NextToken0')
    ->build();
```



