# Inbound Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkluYm91bmRSdWxl

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`InboundRule`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ports` | `String` | Required | The ports on which traffic will be allowed specified as a string containing a single port, a range (e.g. "8000-9000"), or "0" when all ports are open for a protocol. For ICMP rules this parameter will always return "0". |
| `protocol` | [`Protocol`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/protocol.md) | Required | The type of traffic to be allowed. This may be one of `tcp`, `udp`, or `icmp`. |
| `sources` | [`Sources`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/sources.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
inbound_rule = InboundRule.new(
  ports: '8000',
  protocol: Protocol::TCP,
  sources: Sources.new(
    addresses: [
      '1.2.3.4',
      '18.0.0.0/8'
    ],
    droplet_ids: [
      8043964
    ],
    kubernetes_ids: [
      '41b74c5d-9bd0-5555-5555-a57c495b81a3'
    ],
    load_balancer_uids: [
      '4de7ac8b-495b-4884-9a69-1050c6793cd6'
    ],
    tags: [
      'tags1',
      'tags2',
      'tags3'
    ],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



