# Set Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNldFJ1bGVzUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`SetRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `rules` | [`Array[Rule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/rule.md) | Required | Array of rules<br><br>**Constraints**: *Maximum Items*: `50` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
set_rules_request = SetRulesRequest.new(
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
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



