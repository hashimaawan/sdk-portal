# Column Info

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNvbHVtbkluZm8

Information about the columns in a query execution result.


# Class Name

`ColumnInfo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_name` | `String` | Optional | - |
| `schema_name` | `String` | Optional | - |
| `table_name` | `String` | Optional | - |
| `name` | `String` | Required | - |
| `label` | `String` | Optional | - |
| `type` | `String` | Required | - |
| `precision` | `Integer` | Optional | - |
| `scale` | `Integer` | Optional | - |
| `nullable` | [`ColumnNullable2Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/column-nullable-2.md) | Optional | - |
| `case_sensitive` | `TrueClass \| FalseClass` | Optional | - |


# Example

```ruby
column_info = ColumnInfo.new(
  'Name8',
  'Type8',
  'CatalogName2',
  'SchemaName8',
  'TableName4',
  'Label6',
  110,
  nil,
  envrr
)
```



