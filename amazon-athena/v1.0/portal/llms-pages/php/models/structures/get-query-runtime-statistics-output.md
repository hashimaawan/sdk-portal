# Get Query Runtime Statistics Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFF1ZXJ5UnVudGltZVN0YXRpc3RpY3NPdXRwdXQ


# Class Name

`GetQueryRuntimeStatisticsOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryRuntimeStatistics` | [`?QueryRuntimeStatistics2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/query-runtime-statistics-2.md) | Optional | - | getQueryRuntimeStatistics(): ?QueryRuntimeStatistics2 | setQueryRuntimeStatistics(?QueryRuntimeStatistics2 queryRuntimeStatistics): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetQueryRuntimeStatisticsOutputBuilder;
use AmazonAthenaLib\Models\Builders\QueryRuntimeStatistics2Builder;
use AmazonAthenaLib\Models\Builders\QueryRuntimeStatisticsTimelineBuilder;
use AmazonAthenaLib\Models\Builders\QueryRuntimeStatisticsRowsBuilder;
use AmazonAthenaLib\Models\Builders\OutputStageBuilder;

$getQueryRuntimeStatisticsOutput = GetQueryRuntimeStatisticsOutputBuilder::init()
    ->queryRuntimeStatistics(
        QueryRuntimeStatistics2Builder::init()
            ->timeline(
                QueryRuntimeStatisticsTimelineBuilder::init()
                    ->queryQueueTimeInMillis(156)
                    ->queryPlanningTimeInMillis(82)
                    ->engineExecutionTimeInMillis(112)
                    ->serviceProcessingTimeInMillis(126)
                    ->totalExecutionTimeInMillis(106)
                    ->build()
            )
            ->rows(
                QueryRuntimeStatisticsRowsBuilder::init()
                    ->inputRows(230)
                    ->inputBytes(250)
                    ->outputBytes(36)
                    ->outputRows(230)
                    ->build()
            )
            ->outputStage(
                OutputStageBuilder::init()
                    ->stageId(130)
                    ->state('State0')
                    ->outputBytes(108)
                    ->outputRows(158)
                    ->inputBytes(190)
                    ->build()
            )
            ->build()
    )
    ->build();
```



