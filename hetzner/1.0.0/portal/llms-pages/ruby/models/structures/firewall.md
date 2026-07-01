# Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkZpcmV3YWxs

*This model accepts additional fields of type Object.*


# Class Name

`Firewall`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applied_to` | [`Array[AppliedTo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/applied-to.md) | Required | - |
| `created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `id` | `Integer` | Required | ID of the Resource |
| `labels` | `Hash[String, String]` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Required | Name of the Resource. Must be unique per Project. |
| `rules` | [`Array[Rule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/rule.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
firewall = Firewall.new(
  applied_to: [
    AppliedTo.new(
      type: Type6::SERVER,
      applied_to_resources: [
        AppliedToResource.new(
          server: Server.new(
            id: 14,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          type: Type5::SERVER,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      label_selector: LabelSelector.new(
        selector: 'selector8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      server: Server.new(
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
  created: '2016-01-30T23:55:00+00:00',
  id: 42,
  name: 'my-resource',
  rules: [
    Rule.new(
      direction: Direction::ENUM_IN,
      protocol: Protocol::UDP,
      description: 'description2',
      destination_ips: [
        '28.239.13.1/32',
        '28.239.14.0/24',
        'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
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
  labels: {
    'key0' => 'labels2',
    'key1' => 'labels1'
  },
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



