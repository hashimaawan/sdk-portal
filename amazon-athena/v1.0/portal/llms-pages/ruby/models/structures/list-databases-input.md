# List Databases Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3REYXRhYmFzZXNJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`ListDatabasesInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 50` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_databases_input = ListDatabasesInput.new(
  catalog_name: 'CatalogName0',
  next_token: 'NextToken6',
  max_results: 2,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



