# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc291cmNl

*This model accepts additional fields of type Object.*


# Class Name

`Resource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Required | ID of the Resource |
| `type` | `String` | Required | Type of resource referenced |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
resource = Resource.new(
  id: 42,
  type: 'server',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



