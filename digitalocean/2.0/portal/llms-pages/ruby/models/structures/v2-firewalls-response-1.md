# V2 Firewalls Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2FirewallsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewall` | [`Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/firewall.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_firewalls_response1 = V2FirewallsResponse1.new(
  firewall: Firewall.new(
    created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    droplet_ids: [
      67
    ],
    id: 'id6',
    name: 'name6',
    pending_changes: [
      nil,
      PendingChange.new,
      PendingChange.new
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



