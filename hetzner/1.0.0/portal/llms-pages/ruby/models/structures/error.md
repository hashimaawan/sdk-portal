# Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkVycm9y

Error message for the Action if error occurred, otherwise null


# Class Name

`Error`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code` | `String` | Required | Fixed machine readable code |
| `message` | `String` | Required | Humanized error message |


# Example

```ruby
error = Error.new(
  'action_failed',
  'Action failed'
)
```



