# Get Query Runtime Statistics Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFF1ZXJ5UnVudGltZVN0YXRpc3RpY3NJbnB1dA


# Class Name

`GetQueryRuntimeStatisticsInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getQueryExecutionId(): string | setQueryExecutionId(string queryExecutionId): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetQueryRuntimeStatisticsInputBuilder;

$getQueryRuntimeStatisticsInput = GetQueryRuntimeStatisticsInputBuilder::init(
    'QueryExecutionId0'
)->build();
```



