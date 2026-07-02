# Column Info

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNvbHVtbkluZm8

Information about the columns in a query execution result.

*This model accepts additional fields of type Object.*


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
| `nullable` | [`ColumnNullable2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/column-nullable-2.md) | Optional | - |
| `case_sensitive` | `TrueClass \| FalseClass` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
column_info = ColumnInfo.new(
  name: 'Name8',
  type: 'Type8',
  catalog_name: 'CatalogName2',
  schema_name: 'SchemaName8',
  table_name: 'TableName4',
  label: 'Label6',
  precision: 110,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



