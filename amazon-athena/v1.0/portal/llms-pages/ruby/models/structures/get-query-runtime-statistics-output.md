# Get Query Runtime Statistics Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFF1ZXJ5UnVudGltZVN0YXRpc3RpY3NPdXRwdXQ


# Class Name

`GetQueryRuntimeStatisticsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_runtime_statistics` | [`QueryRuntimeStatistics2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-runtime-statistics-2.md) | Optional | - |


# Example

```ruby
get_query_runtime_statistics_output = GetQueryRuntimeStatisticsOutput.new(
  QueryRuntimeStatistics2.new(
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
)
```



