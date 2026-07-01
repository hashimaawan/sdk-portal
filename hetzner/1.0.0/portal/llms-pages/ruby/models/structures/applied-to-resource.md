# Applied to Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkFwcGxpZWRUb1Jlc291cmNl

*This model accepts additional fields of type Object.*


# Class Name

`AppliedToResource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server` | [`Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/server.md) | Optional | - |
| `type` | [`Type5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-5.md) | Optional | Type of resource referenced |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
applied_to_resource = AppliedToResource.new(
  server: Server.new(
    id: 14,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  type: Type5::SERVER,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



