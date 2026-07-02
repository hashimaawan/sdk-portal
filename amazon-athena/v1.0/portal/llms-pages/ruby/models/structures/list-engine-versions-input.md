# List Engine Versions Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc0lucHV0

*This model accepts additional fields of type Object.*


# Class Name

`ListEngineVersionsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 10` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_engine_versions_input = ListEngineVersionsInput.new(
  next_token: 'NextToken0',
  max_results: 10,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



