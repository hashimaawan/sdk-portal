# Get Database Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldERhdGFiYXNlSW5wdXQ


# Class Name

`GetDatabaseInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `catalogName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getCatalogName(): string | setCatalogName(string catalogName): void |
| `databaseName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getDatabaseName(): string | setDatabaseName(string databaseName): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetDatabaseInputBuilder;

$getDatabaseInput = GetDatabaseInputBuilder::init(
    'CatalogName2',
    'DatabaseName2'
)->build();
```



