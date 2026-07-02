# Get Query Results Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFF1ZXJ5UmVzdWx0c091dHB1dA


# Class Name

`GetQueryResultsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `update_count` | `Integer` | Optional | - |
| `result_set` | [`ResultSet2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-set-2.md) | Optional | - |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ruby
get_query_results_output = GetQueryResultsOutput.new(
  242,
  ResultSet2.new(
    [
      Row.new(
        [
          Datum.new(
            'VarCharValue8'
          ),
          Datum.new(
            'VarCharValue8'
          )
        ]
      ),
      Row.new(
        [
          Datum.new(
            'VarCharValue8'
          ),
          Datum.new(
            'VarCharValue8'
          )
        ]
      )
    ],
    ResultSetMetadata2.new(
      [
        ColumnInfo.new(
          'Name6',
          'Type6',
          'CatalogName0',
          'SchemaName0',
          'TableName2',
          'Label4',
          48,
          nil,
          envrr
        )
      ]
    )
  ),
  'NextToken0'
)
```



