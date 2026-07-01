# Add Target Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkFkZFRhcmdldFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`AddTargetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip` | [`Ip`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. |
| `label_selector` | [`LabelSelector12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/label-selector-12.md) | Optional | Configuration for label selector targets, required if type is `label_selector` |
| `server` | [`Server16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/server-16.md) | Optional | Configuration for type Server, required if type is `server` |
| `type` | [`Type29`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-29.md) | Required | Type of the resource |
| `use_private_ip` | `TrueClass \| FalseClass` | Optional | Use the private network IP instead of the public IP of the Server, requires the Server and Load Balancer to be in the same network. Default value is false. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
add_target_request = AddTargetRequest.new(
  type: Type29::SERVER,
  ip: Ip.new(
    ip: 'ip8',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  label_selector: LabelSelector12.new(
    selector: 'selector8',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  server: Server16.new(
    id: 217.74
  ),
  use_private_ip: true,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



