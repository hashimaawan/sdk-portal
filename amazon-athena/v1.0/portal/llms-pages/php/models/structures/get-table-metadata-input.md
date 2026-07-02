# Get Table Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFJbnB1dA


# Class Name

`GetTableMetadataInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `catalogName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getCatalogName(): string | setCatalogName(string catalogName): void |
| `databaseName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getDatabaseName(): string | setDatabaseName(string databaseName): void |
| `tableName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getTableName(): string | setTableName(string tableName): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetTableMetadataInputBuilder;

$getTableMetadataInput = GetTableMetadataInputBuilder::init(
    'CatalogName2',
    'DatabaseName2',
    'TableName4'
)->build();
```



