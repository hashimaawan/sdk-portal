# Batch Get Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25JbnB1dA

Contains an array of query execution IDs.


# Class Name

`BatchGetQueryExecutionInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryExecutionIds` | `string[]` | Required | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getQueryExecutionIds(): array | setQueryExecutionIds(array queryExecutionIds): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\BatchGetQueryExecutionInputBuilder;

$batchGetQueryExecutionInput = BatchGetQueryExecutionInputBuilder::init(
    [
        'QueryExecutionIds7',
        'QueryExecutionIds8',
        'QueryExecutionIds9'
    ]
)->build();
```



