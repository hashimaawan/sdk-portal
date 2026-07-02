# Create Prepared Statement Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZVByZXBhcmVkU3RhdGVtZW50SW5wdXQ


# Class Name

`CreatePreparedStatementInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `statementName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` | getStatementName(): string | setStatementName(string statementName): void |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): string | setWorkGroup(string workGroup): void |
| `queryStatement` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` | getQueryStatement(): string | setQueryStatement(string queryStatement): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\CreatePreparedStatementInputBuilder;

$createPreparedStatementInput = CreatePreparedStatementInputBuilder::init(
    'StatementName2',
    'WorkGroup6',
    'QueryStatement6'
)
    ->description('Description2')
    ->build();
```



