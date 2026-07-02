# Get Query Results Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFF1ZXJ5UmVzdWx0c0lucHV0


# Class Name

`GetQueryResultsInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getQueryExecutionId(): string | setQueryExecutionId(string queryExecutionId): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 1`, `<= 1000` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetQueryResultsInputBuilder;

$getQueryResultsInput = GetQueryResultsInputBuilder::init(
    'QueryExecutionId6'
)
    ->nextToken('NextToken2')
    ->maxResults(42)
    ->build();
```



