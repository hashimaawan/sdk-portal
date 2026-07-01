# Applied To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkFwcGxpZWRUbw

*This model accepts additional fields of type Object.*


# Class Name

`AppliedTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applied_to_resources` | [`Array[AppliedToResource]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/applied-to-resource.md) | Optional | - |
| `label_selector` | [`LabelSelector`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/label-selector.md) | Optional | - |
| `server` | [`Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/server.md) | Optional | - |
| `type` | [`Type6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-6.md) | Required | Type of resource referenced |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
applied_to = AppliedTo.new(
  type: Type6::SERVER,
  applied_to_resources: [
    AppliedToResource.new(
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
  ],
  label_selector: LabelSelector.new(
    selector: 'selector8',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  server: Server.new(
    id: 14,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



