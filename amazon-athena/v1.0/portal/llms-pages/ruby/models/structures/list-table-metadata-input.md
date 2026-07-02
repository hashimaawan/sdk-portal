# List Table Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`ListTableMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `database_name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `expression` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `256` |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 50` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_table_metadata_input = ListTableMetadataInput.new(
  catalog_name: 'CatalogName2',
  database_name: 'DatabaseName2',
  expression: 'Expression0',
  next_token: 'NextToken8',
  max_results: 50,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



