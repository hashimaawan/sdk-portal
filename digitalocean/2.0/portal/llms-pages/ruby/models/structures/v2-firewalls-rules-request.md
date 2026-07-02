# V2 Firewalls Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJ1bGVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2FirewallsRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `inbound_rules` | [`Array[InboundRule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/inbound-rule.md) | Required | - |
| `outbound_rules` | [`Array[OutboundRule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/outbound-rule.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_firewalls_rules_request = V2FirewallsRulesRequest.new(
  inbound_rules: [
    InboundRule.new(
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
  ],
  outbound_rules: [
    OutboundRule.new(
      ports: '8000',
      protocol: Protocol::TCP,
      destinations: Destinations.new(
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
          'tags7',
          'tags8',
          'tags9'
        ],
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



