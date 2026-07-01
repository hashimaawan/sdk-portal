# Servers Actions Change Dns Ptr Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwRG5zJTI1MjBQdHIlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`ServersActionsChangeDnsPtrRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `String` | Required | Hostname to set as a reverse DNS PTR entry, reset to original value if `null` |
| `ip` | `String` | Required | Primary IP address for which the reverse DNS entry should be set |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
servers_actions_change_dns_ptr_request = ServersActionsChangeDnsPtrRequest.new(
  dns_ptr: 'server01.example.com',
  ip: '1.2.3.4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



