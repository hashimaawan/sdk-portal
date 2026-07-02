# Result Set 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlJlc3VsdFNldDI


# Class Name

`ResultSet2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `rows` | [`?(Row[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/row.md) | Optional | - | getRows(): ?array | setRows(?array rows): void |
| `resultSetMetadata` | [`?ResultSetMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/result-set-metadata-2.md) | Optional | - | getResultSetMetadata(): ?ResultSetMetadata2 | setResultSetMetadata(?ResultSetMetadata2 resultSetMetadata): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ResultSet2Builder;
use AmazonAthenaLib\Models\Builders\RowBuilder;
use AmazonAthenaLib\Models\Builders\DatumBuilder;
use AmazonAthenaLib\Models\Builders\ResultSetMetadata2Builder;
use AmazonAthenaLib\Models\Builders\ColumnInfoBuilder;

$resultSet2 = ResultSet2Builder::init()
    ->rows(
        [
            RowBuilder::init()
                ->data(
                    [
                        DatumBuilder::init()
                            ->varCharValue('VarCharValue8')
                            ->build(),
                        DatumBuilder::init()
                            ->varCharValue('VarCharValue8')
                            ->build()
                    ]
                )
                ->build()
        ]
    )
    ->resultSetMetadata(
        ResultSetMetadata2Builder::init()
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
                        ->build()
                ]
            )
            ->build()
    )
    ->build();
```



