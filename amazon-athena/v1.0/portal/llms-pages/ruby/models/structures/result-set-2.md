# Result Set 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdFNldDI

*This model accepts additional fields of type Object.*


# Class Name

`ResultSet2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `rows` | [`Array[Row]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/row.md) | Optional | - |
| `result_set_metadata` | [`ResultSetMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-set-metadata-2.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
result_set2 = ResultSet2.new(
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
)
```



