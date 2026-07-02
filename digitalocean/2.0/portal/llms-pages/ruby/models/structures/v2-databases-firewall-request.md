# V2 Databases Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMEZpcmV3YWxsJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DatabasesFirewallRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `rules` | [`Array[Rule1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/rule-1.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_databases_firewall_request = V2DatabasesFirewallRequest.new(
  rules: [
    Rule1.new(
      type: Type7::IP_ADDR,
      value: 'value0',
      cluster_uuid: 'cluster_uuid4',
      created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      uuid: 'uuid4',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Rule1.new(
      type: Type7::IP_ADDR,
      value: 'value0',
      cluster_uuid: 'cluster_uuid4',
      created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      uuid: 'uuid4',
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



