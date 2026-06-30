# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlJlc291cmNl


# Class Name

`Resource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Required | ID of the Resource |
| `type` | `String` | Required | Type of resource referenced |


# Example

```ruby
resource = Resource.new(
  42,
  'server'
)
```



