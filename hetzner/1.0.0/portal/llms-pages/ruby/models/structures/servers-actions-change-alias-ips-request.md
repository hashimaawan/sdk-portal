# Servers Actions Change Alias Ips Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwQWxpYXMlMjUyMElwcyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`ServersActionsChangeAliasIpsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alias_ips` | `Array[String]` | Required | New alias IPs to set for this Server |
| `network` | `Integer` | Required | ID of an existing Network already attached to the Server |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
servers_actions_change_alias_ips_request = ServersActionsChangeAliasIpsRequest.new(
  alias_ips: [
    '10.0.1.2'
  ],
  network: 4711,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



