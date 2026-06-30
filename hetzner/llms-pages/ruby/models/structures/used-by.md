# Used By

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlVzZWRCeQ


# Class Name

`UsedBy`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Required | ID of resource referenced |
| `type` | `String` | Required | Type of resource referenced |


# Example

```ruby
used_by = UsedBy.new(
  4711,
  'load_balancer'
)
```



