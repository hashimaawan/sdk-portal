# Get Query Results Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFF1ZXJ5UmVzdWx0c091dHB1dA

*This model accepts additional fields of type Object.*


# Class Name

`GetQueryResultsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `update_count` | `Integer` | Optional | - |
| `result_set` | [`ResultSet2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-set-2.md) | Optional | - |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_query_results_output = GetQueryResultsOutput.new(
  update_count: 242,
  result_set: ResultSet2.new(
    rows: [
      Row.new(
        data: [
          Datum.new(
            var_char_value: 'VarCharValue8',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          Datum.new(
            var_char_value: 'VarCharValue8',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Row.new(
        data: [
          Datum.new(
            var_char_value: 'VarCharValue8',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          Datum.new(
            var_char_value: 'VarCharValue8',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    result_set_metadata: ResultSetMetadata2.new(
      column_info: [
        ColumnInfo.new(
          name: 'Name6',
          type: 'Type6',
          catalog_name: 'CatalogName0',
          schema_name: 'SchemaName0',
          table_name: 'TableName2',
          label: 'Label4',
          precision: 48,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  next_token: 'NextToken0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



