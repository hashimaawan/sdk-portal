# List Data Catalogs Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`ListDataCatalogsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `Integer` | Optional | **Constraints**: `>= 2`, `<= 50` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_data_catalogs_input = ListDataCatalogsInput.new(
  next_token: 'NextToken4',
  max_results: 50,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



