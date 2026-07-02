# Get Database Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldERhdGFiYXNlSW5wdXQ


# Class Name

`GetDatabaseInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `database_name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |


# Example

```ruby
get_database_input = GetDatabaseInput.new(
  'CatalogName4',
  'DatabaseName4'
)
```



