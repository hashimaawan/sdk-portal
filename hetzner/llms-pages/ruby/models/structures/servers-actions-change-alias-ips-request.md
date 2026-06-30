# Servers Actions Change Alias Ips Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwQWxpYXMlMjUyMElwcyUyNTIwUmVxdWVzdA


# Class Name

`ServersActionsChangeAliasIpsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alias_ips` | `Array[String]` | Required | New alias IPs to set for this Server |
| `network` | `Integer` | Required | ID of an existing Network already attached to the Server |


# Example

```ruby
servers_actions_change_alias_ips_request = ServersActionsChangeAliasIpsRequest.new(
  [
    '10.0.1.2'
  ],
  4711
)
```



