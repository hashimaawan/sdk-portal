# V2 Load Balancers Forwarding Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMEZvcndhcmRpbmclMjUyMFJ1bGVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2LoadBalancersForwardingRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `forwarding_rules` | [`Array[ForwardingRule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/forwarding-rule.md) | Required | **Constraints**: *Minimum Items*: `1` |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_load_balancers_forwarding_rules_request = V2LoadBalancersForwardingRulesRequest.new(
  forwarding_rules: [
    ForwardingRule.new(
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
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



