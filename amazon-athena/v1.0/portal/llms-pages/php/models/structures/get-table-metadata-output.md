# Get Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFPdXRwdXQ

*This model accepts additional fields of type array.*


# Class Name

`GetTableMetadataOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `tableMetadata` | [`?TableMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/table-metadata-2.md) | Optional | - | getTableMetadata(): ?TableMetadata2 | setTableMetadata(?TableMetadata2 tableMetadata): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetTableMetadataOutputBuilder;
use AmazonAthenaLib\Models\Builders\TableMetadata2Builder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\Builders\ColumnBuilder;
use AmazonAthenaLib\ApiHelper;

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
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    ColumnBuilder::init(
                        'Name0'
                    )
                        ->type('Type0')
                        ->comment('Comment4')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
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
                        ->build()
                ]
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



