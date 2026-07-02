# Query Execution Context

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uQ29udGV4dA

The database and data catalog context in which the query execution occurs.

*This model accepts additional fields of type array.*


# Class Name

`QueryExecutionContext`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `database` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | getDatabase(): ?string | setDatabase(?string database): void |
| `catalog` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getCatalog(): ?string | setCatalog(?string catalog): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\QueryExecutionContextBuilder;
use AmazonAthenaLib\ApiHelper;

$queryExecutionContext = QueryExecutionContextBuilder::init()
    ->database('Database0')
    ->catalog('Catalog6')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



