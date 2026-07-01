# Apply to Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkFwcGx5VG9SZXNvdXJjZXNSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`ApplyToResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `apply_to` | [`Array[FirewallApplyToResources]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/firewall-apply-to-resources.md) | Required | Resources the Firewall should be applied to |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
apply_to_resources_request = ApplyToResourcesRequest.new(
  apply_to: [
    FirewallApplyToResources.new(
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
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



