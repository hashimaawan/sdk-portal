# Applied To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkFwcGxpZWRUbw


# Class Name

`AppliedTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applied_to_resources` | [`Array[AppliedToResource]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/applied-to-resource.md) | Optional | - |
| `label_selector` | [`LabelSelector`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/label-selector.md) | Optional | - |
| `server` | [`Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/server.md) | Optional | - |
| `type` | [`Type6Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/type-6.md) | Required | Type of resource referenced |


# Example

```ruby
applied_to = AppliedTo.new(
  Type6Enum::SERVER,
  [
    AppliedToResource.new(
      Server.new(
        14
      ),
      Type5Enum::SERVER
    )
  ],
  LabelSelector.new(
    'selector8'
  ),
  Server.new(
    14
  )
)
```



