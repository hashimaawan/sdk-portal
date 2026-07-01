# Used By

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlVzZWRCeQ

*This model accepts additional fields of type Object.*


# Class Name

`UsedBy`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Required | ID of resource referenced |
| `type` | `String` | Required | Type of resource referenced |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
used_by = UsedBy.new(
  id: 4711,
  type: 'load_balancer',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



