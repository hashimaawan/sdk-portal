# Server Public Net Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlclB1YmxpY05ldEZpcmV3YWxs

*This model accepts additional fields of type Object.*


# Class Name

`ServerPublicNetFirewall`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Optional | ID of the Resource |
| `status` | [`Status72`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/status-72.md) | Optional | Status of the Firewall on the Server |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
server_public_net_firewall = ServerPublicNetFirewall.new(
  id: 42,
  status: Status72::APPLIED,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



