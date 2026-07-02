# Get Table Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`GetTableMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `database_name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `table_name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_table_metadata_input = GetTableMetadataInput.new(
  catalog_name: 'CatalogName4',
  database_name: 'DatabaseName4',
  table_name: 'TableName6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



