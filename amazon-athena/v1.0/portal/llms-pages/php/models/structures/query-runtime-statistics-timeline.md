# Query Runtime Statistics Timeline

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3NUaW1lbGluZQ

Timeline statistics such as query queue time, planning time, execution time, service processing time, and total execution time.

*This model accepts additional fields of type array.*


# Class Name

`QueryRuntimeStatisticsTimeline`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryQueueTimeInMillis` | `?int` | Optional | - | getQueryQueueTimeInMillis(): ?int | setQueryQueueTimeInMillis(?int queryQueueTimeInMillis): void |
| `queryPlanningTimeInMillis` | `?int` | Optional | - | getQueryPlanningTimeInMillis(): ?int | setQueryPlanningTimeInMillis(?int queryPlanningTimeInMillis): void |
| `engineExecutionTimeInMillis` | `?int` | Optional | - | getEngineExecutionTimeInMillis(): ?int | setEngineExecutionTimeInMillis(?int engineExecutionTimeInMillis): void |
| `serviceProcessingTimeInMillis` | `?int` | Optional | - | getServiceProcessingTimeInMillis(): ?int | setServiceProcessingTimeInMillis(?int serviceProcessingTimeInMillis): void |
| `totalExecutionTimeInMillis` | `?int` | Optional | - | getTotalExecutionTimeInMillis(): ?int | setTotalExecutionTimeInMillis(?int totalExecutionTimeInMillis): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\QueryRuntimeStatisticsTimelineBuilder;
use AmazonAthenaLib\ApiHelper;

$queryRuntimeStatisticsTimeline = QueryRuntimeStatisticsTimelineBuilder::init()
    ->queryQueueTimeInMillis(122)
    ->queryPlanningTimeInMillis(48)
    ->engineExecutionTimeInMillis(78)
    ->serviceProcessingTimeInMillis(96)
    ->totalExecutionTimeInMillis(140)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



