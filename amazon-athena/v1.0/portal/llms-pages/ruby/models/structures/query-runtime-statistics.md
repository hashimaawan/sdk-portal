# Query Runtime Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3M

The query execution timeline, statistics on input and output rows and bytes, and the different query stages that form the query execution plan.


# Class Name

`QueryRuntimeStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `timeline` | [`QueryRuntimeStatisticsTimeline`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-runtime-statistics-timeline.md) | Optional | Timeline statistics such as query queue time, planning time, execution time, service processing time, and total execution time. |
| `rows` | [`QueryRuntimeStatisticsRows`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-runtime-statistics-rows.md) | Optional | Statistics such as input rows and bytes read by the query, rows and bytes output by the query, and the number of rows written by the query. |
| `output_stage` | [`OutputStage`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/output-stage.md) | Optional | - |


# Example

```ruby
query_runtime_statistics = QueryRuntimeStatistics.new(
  QueryRuntimeStatisticsTimeline.new(
    156,
    82,
    112,
    126,
    106
  ),
  QueryRuntimeStatisticsRows.new(
    230,
    250,
    36,
    230
  ),
  OutputStage.new(
    130,
    'State0',
    108,
    158,
    190,
    nil,
    nil,
    QueryStagePlan.new(
      nil,
      nil,
      [],
      []
    ),
    []
  )
)
```



