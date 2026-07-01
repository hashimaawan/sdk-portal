# Firewalls Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkZpcmV3YWxsc1Jlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`FirewallsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewalls` | [`Array[Firewall]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/firewall.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/meta.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
firewalls_response = FirewallsResponse.new(
  firewalls: [
    Firewall.new(
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
        'key0' => 'labels4',
        'key1' => 'labels5'
      },
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  meta: Meta.new(
    pagination: Pagination.new(
      last_page: 77.7,
      next_page: 209.18,
      page: 17.58,
      per_page: 13.34,
      previous_page: 50.02,
      total_entries: 206.64,
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



