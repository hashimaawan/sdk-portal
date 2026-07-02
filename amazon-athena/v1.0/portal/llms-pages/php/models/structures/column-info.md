# Column Info

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkNvbHVtbkluZm8

Information about the columns in a query execution result.

*This model accepts additional fields of type array.*


# Class Name

`ColumnInfo`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `catalogName` | `?string` | Optional | - | getCatalogName(): ?string | setCatalogName(?string catalogName): void |
| `schemaName` | `?string` | Optional | - | getSchemaName(): ?string | setSchemaName(?string schemaName): void |
| `tableName` | `?string` | Optional | - | getTableName(): ?string | setTableName(?string tableName): void |
| `name` | `string` | Required | - | getName(): string | setName(string name): void |
| `label` | `?string` | Optional | - | getLabel(): ?string | setLabel(?string label): void |
| `type` | `string` | Required | - | getType(): string | setType(string type): void |
| `precision` | `?int` | Optional | - | getPrecision(): ?int | setPrecision(?int precision): void |
| `scale` | `?int` | Optional | - | getScale(): ?int | setScale(?int scale): void |
| `nullable` | [`?string(ColumnNullable2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/column-nullable-2.md) | Optional | - | getNullable(): ?string | setNullable(?string nullable): void |
| `caseSensitive` | `?bool` | Optional | - | getCaseSensitive(): ?bool | setCaseSensitive(?bool caseSensitive): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ColumnInfoBuilder;
use AmazonAthenaLib\ApiHelper;

$columnInfo = ColumnInfoBuilder::init(
    'Name8',
    'Type8'
)
    ->catalogName('CatalogName2')
    ->schemaName('SchemaName2')
    ->tableName('TableName4')
    ->label('Label6')
    ->precision(196)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



