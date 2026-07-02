# Query Execution Context

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uQ29udGV4dA

The database and data catalog context in which the query execution occurs.


# Class Name

`QueryExecutionContext`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `database` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | getDatabase(): ?string | setDatabase(?string database): void |
| `catalog` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getCatalog(): ?string | setCatalog(?string catalog): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\QueryExecutionContextBuilder;

$queryExecutionContext = QueryExecutionContextBuilder::init()
    ->database('Database0')
    ->catalog('Catalog6')
    ->build();
```



