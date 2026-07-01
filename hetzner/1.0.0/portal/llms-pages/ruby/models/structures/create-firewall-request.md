# Create Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`CreateFirewallRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `apply_to` | [`Array[ApplyTo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/apply-to.md) | Optional | Resources the Firewall should be applied to after creation |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Required | Name of the Firewall |
| `rules` | [`Array[Rule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/rule.md) | Optional | Array of rules |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
create_firewall_request = CreateFirewallRequest.new(
  name: 'Corporate Intranet Protection',
  apply_to: [
    ApplyTo.new(
      type: Type7::SERVER,
      label_selector: LabelSelector1.new(
        selector: 'selector8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      server: Server2.new(
        id: 14,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    ApplyTo.new(
      type: Type7::SERVER,
      label_selector: LabelSelector1.new(
        selector: 'selector8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      server: Server2.new(
        id: 14,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    ApplyTo.new(
      type: Type7::SERVER,
      label_selector: LabelSelector1.new(
        selector: 'selector8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      server: Server2.new(
        id: 14,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  labels: { 'key1' => 'val1', 'key2' => 'val2' },
  rules: [
    Rule.new(
      direction: Direction::ENUM_IN,
      protocol: Protocol::TCP,
      description: 'description2',
      destination_ips: [
        'destination_ips1',
        'destination_ips2',
        'destination_ips3'
      ],
      port: '80',
      source_ips: [
        '28.239.13.1/32',
        '28.239.14.0/24',
        'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
      ],
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



