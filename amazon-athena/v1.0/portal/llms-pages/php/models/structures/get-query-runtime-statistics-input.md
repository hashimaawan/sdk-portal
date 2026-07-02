# Get Query Runtime Statistics Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFF1ZXJ5UnVudGltZVN0YXRpc3RpY3NJbnB1dA

*This model accepts additional fields of type array.*


# Class Name

`GetQueryRuntimeStatisticsInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getQueryExecutionId(): string | setQueryExecutionId(string queryExecutionId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetQueryRuntimeStatisticsInputBuilder;
use AmazonAthenaLib\ApiHelper;

$getQueryRuntimeStatisticsInput = GetQueryRuntimeStatisticsInputBuilder::init(
    'QueryExecutionId0'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



