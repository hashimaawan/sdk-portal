# Applied to Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkFwcGxpZWRUb1Jlc291cmNl


# Class Name

`AppliedToResource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server` | [`Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/server.md) | Optional | - |
| `type` | [`Type5Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/type-5.md) | Optional | Type of resource referenced |


# Example

```ruby
applied_to_resource = AppliedToResource.new(
  Server.new(
    14
  ),
  Type5Enum::SERVER
)
```



