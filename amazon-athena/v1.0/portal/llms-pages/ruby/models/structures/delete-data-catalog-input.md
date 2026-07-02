# Delete Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkRlbGV0ZURhdGFDYXRhbG9nSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`DeleteDataCatalogInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
delete_data_catalog_input = DeleteDataCatalogInput.new(
  name: 'Name2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



