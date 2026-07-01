# Remove from Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlbW92ZUZyb21SZXNvdXJjZXNSZXF1ZXN0


# Class Name

`RemoveFromResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `remove_from` | [`Array[FirewallRemoveFromResources]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/firewall-remove-from-resources.md) | Required | Resources the Firewall should be removed from |


# Example

```ruby
remove_from_resources_request = RemoveFromResourcesRequest.new(
  [
    FirewallRemoveFromResources.new(
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



