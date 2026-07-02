# List Query Executions Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RRdWVyeUV4ZWN1dGlvbnNPdXRwdXQ


# Class Name

`ListQueryExecutionsOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryExecutionIds` | `?(string[])` | Optional | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getQueryExecutionIds(): ?array | setQueryExecutionIds(?array queryExecutionIds): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListQueryExecutionsOutputBuilder;

$listQueryExecutionsOutput = ListQueryExecutionsOutputBuilder::init()
    ->queryExecutionIds(
        [
            'QueryExecutionIds9'
        ]
    )
    ->nextToken('NextToken2')
    ->build();
```



