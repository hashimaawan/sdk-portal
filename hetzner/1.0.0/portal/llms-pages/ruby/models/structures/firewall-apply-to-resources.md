# Firewall Apply to Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkZpcmV3YWxsQXBwbHlUb1Jlc291cmNlcw

*This model accepts additional fields of type Object.*


# Class Name

`FirewallApplyToResources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `label_selector` | [`LabelSelector5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/label-selector-5.md) | Optional | Configuration for type label_selector, required if type is `label_selector` |
| `server` | [`Server9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/server-9.md) | Optional | Configuration for type server, required if type is `server` |
| `type` | [`Type7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-7.md) | Optional | Type of the resource |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
firewall_apply_to_resources = FirewallApplyToResources.new(
  label_selector: LabelSelector5.new(
    selector: 'selector8',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  server: Server9.new(
    id: 14,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  type: Type7::SERVER,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



