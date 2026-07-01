# Apply To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkFwcGx5VG8

*This model accepts additional fields of type Object.*


# Class Name

`ApplyTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `label_selector` | [`LabelSelector1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/label-selector-1.md) | Optional | Configuration for type LabelSelector, required if type is `label_selector` |
| `server` | [`Server2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/server-2.md) | Optional | Configuration for type Server, required if type is `server` |
| `type` | [`Type7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-7.md) | Required | Type of the resource |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
apply_to = ApplyTo.new(
  type: Type7::SERVER,
  label_selector: LabelSelector1.new(
    selector: 'selector8',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  server: Server2.new(
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



