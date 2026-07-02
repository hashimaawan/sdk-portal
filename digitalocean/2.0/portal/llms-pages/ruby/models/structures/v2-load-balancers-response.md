# V2 Load Balancers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2LoadBalancersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancers` | [`Array[LoadBalancer1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/load-balancer-1.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_load_balancers_response = V2LoadBalancersResponse.new(
  meta: Meta.new(
    total: 1,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  load_balancers: [
    LoadBalancer1.new(
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
    LoadBalancer1.new(
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
    LoadBalancer1.new(
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
    )
  ],
  links: Links.new(
    pages: Pages.new(
      last: 'last6',
      mnext: 'next2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



