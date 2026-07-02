# Get Table Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFJbnB1dA


# Class Name

`GetTableMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `database_name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `table_name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |


# Example

```ruby
get_table_metadata_input = GetTableMetadataInput.new(
  'CatalogName4',
  'DatabaseName4',
  'TableName6'
)
```



