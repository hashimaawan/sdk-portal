# Table Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlRhYmxlTWV0YWRhdGE

Contains metadata for a table.

*This model accepts additional fields of type Object.*


# Class Name

`TableMetadata`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `create_time` | `DateTime` | Optional | - |
| `last_access_time` | `DateTime` | Optional | - |
| `table_type` | `String` | Optional | **Constraints**: *Maximum Length*: `255` |
| `columns` | [`Array[Column]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/column.md) | Optional | - |
| `partition_keys` | [`Array[Column]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/column.md) | Optional | - |
| `parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/parameters.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
table_metadata = TableMetadata.new(
  name: 'Name0',
  create_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  last_access_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  table_type: 'TableType4',
  columns: [
    Column.new(
      name: 'Name0',
      type: 'Type0',
      comment: 'Comment4',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Column.new(
      name: 'Name0',
      type: 'Type0',
      comment: 'Comment4',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  partition_keys: [
    Column.new(
      name: 'Name6',
      type: 'Type6',
      comment: 'Comment0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Column.new(
      name: 'Name6',
      type: 'Type6',
      comment: 'Comment0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



