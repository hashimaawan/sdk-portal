# Table Metadata 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlRhYmxlTWV0YWRhdGEy


# Class Name

`TableMetadata2`


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


# Example

```ruby
table_metadata2 = TableMetadata2.new(
  'Name6',
  DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  'TableType2',
  [
    Column.new(
      'Name0',
      'Type0',
      'Comment4'
    ),
    Column.new(
      'Name0',
      'Type0',
      'Comment4'
    )
  ],
  [
    Column.new(
      'Name6',
      'Type6',
      'Comment0'
    )
  ],
  Parameters.new
)
```



