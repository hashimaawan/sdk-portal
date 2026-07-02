# Result Set

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlJlc3VsdFNldA

The metadata and rows that make up a query result set. The metadata describes the column structure and data types. To return a <code>ResultSet</code> object, use <a>GetQueryResults</a>.

*This model accepts additional fields of type array.*


# Class Name

`ResultSet`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `rows` | [`?(Row[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/row.md) | Optional | - | getRows(): ?array | setRows(?array rows): void |
| `resultSetMetadata` | [`?ResultSetMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/result-set-metadata-2.md) | Optional | - | getResultSetMetadata(): ?ResultSetMetadata2 | setResultSetMetadata(?ResultSetMetadata2 resultSetMetadata): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ResultSetBuilder;
use AmazonAthenaLib\Models\Builders\RowBuilder;
use AmazonAthenaLib\Models\Builders\DatumBuilder;
use AmazonAthenaLib\ApiHelper;
use AmazonAthenaLib\Models\Builders\ResultSetMetadata2Builder;
use AmazonAthenaLib\Models\Builders\ColumnInfoBuilder;

$resultSet = ResultSetBuilder::init()
    ->rows(
        [
            RowBuilder::init()
                ->data(
                    [
                        DatumBuilder::init()
                            ->varCharValue('VarCharValue8')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build(),
                        DatumBuilder::init()
                            ->varCharValue('VarCharValue8')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    ]
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
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



