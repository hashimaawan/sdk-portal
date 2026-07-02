# Start Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXJ0UXVlcnlFeGVjdXRpb25PdXRwdXQ


# Class Name

`StartQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryExecutionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getQueryExecutionId(): ?string | setQueryExecutionId(?string queryExecutionId): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\StartQueryExecutionOutputBuilder;

$startQueryExecutionOutput = StartQueryExecutionOutputBuilder::init()
    ->queryExecutionId('QueryExecutionId0')
    ->build();
```



