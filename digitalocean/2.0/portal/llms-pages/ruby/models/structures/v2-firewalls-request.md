# V2 Firewalls Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2FirewallsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the firewall was created. |
| `droplet_ids` | `Array[Integer]` | Optional | An array containing the IDs of the Droplets assigned to the firewall. |
| `id` | `String` | Optional, Read-only | A unique ID that can be used to identify and reference a firewall. |
| `name` | `String` | Required | A human-readable name for a firewall. The name must begin with an alphanumeric character. Subsequent characters must either be alphanumeric characters, a period (.), or a dash (-).<br><br>**Constraints**: *Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9\.-]+$` |
| `pending_changes` | [`Array[PendingChange]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/pending-change.md) | Optional, Read-only | An array of objects each containing the fields "droplet_id", "removing", and "status". It is provided to detail exactly which Droplets are having their security policies updated. When empty, all changes have been successfully applied. |
| `status` | [`Status9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/status-9.md) | Optional, Read-only | A status string indicating the current state of the firewall. This can be "waiting", "succeeded", or "failed". |
| `tags` | `Array[String]` | Optional | - |
| `inbound_rules` | [`Array[InboundRule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/inbound-rule.md) | Required | - |
| `outbound_rules` | [`Array[OutboundRule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/outbound-rule.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_firewalls_request = V2FirewallsRequest.new(
  name: 'firewall',
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
  created_at: DateTimeHelper.from_rfc3339('2020-05-23T21:24:00Z'),
  droplet_ids: [
    8043964
  ],
  id: 'bb4b2611-3d72-467b-8602-280330ecd65c',
  pending_changes: [
    PendingChange.new(
      droplet_id: 8043964,
      removing: false,
      status: 'waiting',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  status: Status9::WAITING,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



