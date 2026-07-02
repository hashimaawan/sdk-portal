# Query Runtime Statistics Rows

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3NSb3dz

Statistics such as input rows and bytes read by the query, rows and bytes output by the query, and the number of rows written by the query.


# Class Name

`QueryRuntimeStatisticsRows`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `input_rows` | `Integer` | Optional | - |
| `input_bytes` | `Integer` | Optional | - |
| `output_bytes` | `Integer` | Optional | - |
| `output_rows` | `Integer` | Optional | - |


# Example

```ruby
query_runtime_statistics_rows = QueryRuntimeStatisticsRows.new(
  100,
  136,
  94,
  104
)
```



