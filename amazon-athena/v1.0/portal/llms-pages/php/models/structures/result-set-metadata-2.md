# Result Set Metadata 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRhMg


# Class Name

`ResultSetMetadata2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `columnInfo` | [`?(ColumnInfo[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/column-info.md) | Optional | - | getColumnInfo(): ?array | setColumnInfo(?array columnInfo): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ResultSetMetadata2Builder;
use AmazonAthenaLib\Models\Builders\ColumnInfoBuilder;

$resultSetMetadata2 = ResultSetMetadata2Builder::init()
    ->columnInfo(
        [
            ColumnInfoBuilder::init(
                'Name6',
                'Type6'
            )
                ->catalogName('CatalogName0')
                ->schemaName('SchemaName0')
                ->tableName('TableName2')
                ->label('Label4')
                ->precision(48)
                ->build(),
            ColumnInfoBuilder::init(
                'Name6',
                'Type6'
            )
                ->catalogName('CatalogName0')
                ->schemaName('SchemaName0')
                ->tableName('TableName2')
                ->label('Label4')
                ->precision(48)
                ->build()
        ]
    )
    ->build();
```



