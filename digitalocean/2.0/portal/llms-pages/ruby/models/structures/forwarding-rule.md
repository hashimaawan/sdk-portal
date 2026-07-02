# Forwarding Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkZvcndhcmRpbmdSdWxl

An object specifying a forwarding rule for a load balancer.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`ForwardingRule`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate_id` | `String` | Optional | The ID of the TLS certificate used for SSL termination if enabled. |
| `entry_port` | `Integer` | Required | An integer representing the port on which the load balancer instance will listen. |
| `entry_protocol` | [`EntryProtocol`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/entry-protocol.md) | Required | The protocol used for traffic to the load balancer. The possible values are: `http`, `https`, `http2`, `http3`, `tcp`, or `udp`. If you set the  `entry_protocol` to `udp`, the `target_protocol` must be set to `udp`.  When using UDP, the load balancer requires that you set up a health  check with a port that uses TCP, HTTP, or HTTPS to work properly. |
| `target_port` | `Integer` | Required | An integer representing the port on the backend Droplets to which the load balancer will send traffic. |
| `target_protocol` | [`TargetProtocol`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/target-protocol.md) | Required | The protocol used for traffic from the load balancer to the backend Droplets. The possible values are: `http`, `https`, `http2`, `tcp`, or `udp`. If you set the `target_protocol` to `udp`, the `entry_protocol` must be set to  `udp`. When using UDP, the load balancer requires that you set up a health  check with a port that uses TCP, HTTP, or HTTPS to work properly. |
| `tls_passthrough` | `TrueClass \| FalseClass` | Optional | A boolean value indicating whether SSL encrypted traffic will be passed through to the backend Droplets. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
forwarding_rule = ForwardingRule.new(
  entry_port: 443,
  entry_protocol: EntryProtocol::HTTPS,
  target_port: 80,
  target_protocol: TargetProtocol::HTTP,
  certificate_id: '892071a0-bb95-49bc-8021-3afd67a210bf',
  tls_passthrough: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



