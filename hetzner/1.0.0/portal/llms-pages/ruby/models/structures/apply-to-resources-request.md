# Apply to Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkFwcGx5VG9SZXNvdXJjZXNSZXF1ZXN0


# Class Name

`ApplyToResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `apply_to` | [`Array[FirewallApplyToResources]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/firewall-apply-to-resources.md) | Required | Resources the Firewall should be applied to |


# Example

```ruby
apply_to_resources_request = ApplyToResourcesRequest.new(
  [
    FirewallApplyToResources.new(
      LabelSelector5.new(
        'selector8'
      ),
      Server9.new(
        14
      ),
      Type7Enum::SERVER
    )
  ]
)
```



