# Protection 20

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByb3RlY3Rpb24yMA

Protection configuration for the Server


# Class Name

`Protection20`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `TrueClass \| FalseClass` | Required | If true, prevents the Server from being deleted |
| `rebuild` | `TrueClass \| FalseClass` | Required | If true, prevents the Server from being rebuilt |


# Example

```ruby
protection20 = Protection20.new(
  false,
  false
)
```



