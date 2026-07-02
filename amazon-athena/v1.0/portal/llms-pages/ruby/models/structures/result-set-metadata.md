# Result Set Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRh

The metadata that describes the column structure and data types of a table of query results. To return a <code>ResultSetMetadata</code> object, use <a>GetQueryResults</a>.

*This model accepts additional fields of type Object.*


# Class Name

`ResultSetMetadata`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `column_info` | [`Array[ColumnInfo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/column-info.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
result_set_metadata = ResultSetMetadata.new(
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
)
```



