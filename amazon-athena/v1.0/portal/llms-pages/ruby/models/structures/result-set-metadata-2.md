# Result Set Metadata 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRhMg


# Class Name

`ResultSetMetadata2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `column_info` | [`Array[ColumnInfo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/column-info.md) | Optional | - |


# Example

```ruby
result_set_metadata2 = ResultSetMetadata2.new(
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
```



