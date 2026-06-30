# Server Public Net Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlNlcnZlclB1YmxpY05ldEZpcmV3YWxs


# Class Name

`ServerPublicNetFirewall`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Optional | ID of the Resource |
| `status` | [`Status72Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/status-72.md) | Optional | Status of the Firewall on the Server |


# Example

```ruby
server_public_net_firewall = ServerPublicNetFirewall.new(
  42,
  Status72Enum::APPLIED
)
```



