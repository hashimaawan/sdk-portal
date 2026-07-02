# List Table Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhSW5wdXQ


# Class Name

`ListTableMetadataInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `catalogName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getCatalogName(): string | setCatalogName(string catalogName): void |
| `databaseName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getDatabaseName(): string | setDatabaseName(string databaseName): void |
| `expression` | `?string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `256` | getExpression(): ?string | setExpression(?string expression): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 1`, `<= 50` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListTableMetadataInputBuilder;

$listTableMetadataInput = ListTableMetadataInputBuilder::init(
    'CatalogName2',
    'DatabaseName2'
)
    ->expression('Expression0')
    ->nextToken('NextToken8')
    ->maxResults(50)
    ->build();
```



