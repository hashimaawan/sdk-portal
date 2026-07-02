# Get Database Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldERhdGFiYXNlSW5wdXQ

*This model accepts additional fields of type array.*


# Class Name

`GetDatabaseInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `catalogName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getCatalogName(): string | setCatalogName(string catalogName): void |
| `databaseName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getDatabaseName(): string | setDatabaseName(string databaseName): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetDatabaseInputBuilder;
use AmazonAthenaLib\ApiHelper;

$getDatabaseInput = GetDatabaseInputBuilder::init(
    'CatalogName2',
    'DatabaseName2'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



