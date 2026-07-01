# Servers Actions Change Dns Ptr Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwRG5zJTI1MjBQdHIlMjUyMFJlcXVlc3Q


# Class Name

`ServersActionsChangeDnsPtrRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `String` | Required | Hostname to set as a reverse DNS PTR entry, reset to original value if `null` |
| `ip` | `String` | Required | Primary IP address for which the reverse DNS entry should be set |


# Example

```ruby
servers_actions_change_dns_ptr_request = ServersActionsChangeDnsPtrRequest.new(
  'server01.example.com',
  '1.2.3.4'
)
```



