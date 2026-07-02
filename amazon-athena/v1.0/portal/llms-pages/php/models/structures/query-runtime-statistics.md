# Query Runtime Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3M

The query execution timeline, statistics on input and output rows and bytes, and the different query stages that form the query execution plan.


# Class Name

`QueryRuntimeStatistics`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `timeline` | [`?QueryRuntimeStatisticsTimeline`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/query-runtime-statistics-timeline.md) | Optional | Timeline statistics such as query queue time, planning time, execution time, service processing time, and total execution time. | getTimeline(): ?QueryRuntimeStatisticsTimeline | setTimeline(?QueryRuntimeStatisticsTimeline timeline): void |
| `rows` | [`?QueryRuntimeStatisticsRows`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/query-runtime-statistics-rows.md) | Optional | Statistics such as input rows and bytes read by the query, rows and bytes output by the query, and the number of rows written by the query. | getRows(): ?QueryRuntimeStatisticsRows | setRows(?QueryRuntimeStatisticsRows rows): void |
| `outputStage` | [`?OutputStage`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/output-stage.md) | Optional | - | getOutputStage(): ?OutputStage | setOutputStage(?OutputStage outputStage): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\QueryRuntimeStatisticsBuilder;
use AmazonAthenaLib\Models\Builders\QueryRuntimeStatisticsTimelineBuilder;
use AmazonAthenaLib\Models\Builders\QueryRuntimeStatisticsRowsBuilder;
use AmazonAthenaLib\Models\Builders\OutputStageBuilder;

$queryRuntimeStatistics = QueryRuntimeStatisticsBuilder::init()
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
    ->build();
```



