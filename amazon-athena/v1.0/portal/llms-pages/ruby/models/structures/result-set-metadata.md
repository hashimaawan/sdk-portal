# Result Set Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRh

The metadata that describes the column structure and data types of a table of query results. To return a <code>ResultSetMetadata</code> object, use <a>GetQueryResults</a>.


# Class Name

`ResultSetMetadata`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `column_info` | [`Array[ColumnInfo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/column-info.md) | Optional | - |


# Example

```ruby
result_set_metadata = ResultSetMetadata.new(
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



