# V2 Load Balancers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2LoadBalancersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancer` | [`LoadBalancer1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/load-balancer-1.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_load_balancers_response1 = V2LoadBalancersResponse1.new(
  load_balancer: LoadBalancer1.new(
    forwarding_rules: [
      ForwardingRule.new(
        entry_port: 220,
        entry_protocol: EntryProtocol::HTTP2,
        target_port: 104,
        target_protocol: TargetProtocol::HTTPS,
        certificate_id: 'certificate_id4',
        tls_passthrough: false,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      ForwardingRule.new(
        entry_port: 220,
        entry_protocol: EntryProtocol::HTTP2,
        target_port: 104,
        target_protocol: TargetProtocol::HTTPS,
        certificate_id: 'certificate_id4',
        tls_passthrough: false,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    algorithm: Algorithm::ROUND_ROBIN,
    created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    disable_lets_encrypt_dns_records: false,
    enable_backend_keepalive: false,
    enable_proxy_protocol: false,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



