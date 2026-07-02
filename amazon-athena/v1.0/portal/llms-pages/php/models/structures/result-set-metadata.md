# Result Set Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRh

The metadata that describes the column structure and data types of a table of query results. To return a <code>ResultSetMetadata</code> object, use <a>GetQueryResults</a>.

*This model accepts additional fields of type array.*


# Class Name

`ResultSetMetadata`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `columnInfo` | [`?(ColumnInfo[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/column-info.md) | Optional | - | getColumnInfo(): ?array | setColumnInfo(?array columnInfo): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ResultSetMetadataBuilder;
use AmazonAthenaLib\Models\Builders\ColumnInfoBuilder;
use AmazonAthenaLib\ApiHelper;

$resultSetMetadata = ResultSetMetadataBuilder::init()
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
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



