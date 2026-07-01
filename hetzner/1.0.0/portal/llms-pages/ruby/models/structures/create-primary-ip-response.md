# Create Primary IP Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`CreatePrimaryIpResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action.md) | Optional | - |
| `primary_ip` | [`PrimaryIp1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/primary-ip-1.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
create_primary_ip_response = CreatePrimaryIpResponse.new(
  primary_ip: PrimaryIp1.new(
    assignee_id: 17,
    assignee_type: 'server',
    auto_delete: true,
    blocked: false,
    created: '2016-01-30T23:55:00+00:00',
    datacenter: Datacenter2.new(
      description: 'Falkenstein DC Park 8',
      id: 42,
      location: Location.new(
        city: 'Falkenstein',
        country: 'DE',
        description: 'Falkenstein DC Park 1',
        id: 1,
        latitude: 50.47612,
        longitude: 12.370071,
        name: 'fsn1',
        network_zone: 'eu-central',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      name: 'fsn1-dc8',
      server_types: ServerTypes.new(
        available: [
          1,
          2,
          3
        ],
        available_for_migration: [
          1,
          2,
          3
        ],
        supported: [
          1,
          2,
          3
        ],
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    dns_ptr: [
      DnsPtr.new(
        dns_ptr: 'server.example.com',
        ip: '2001:db8::1',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    id: 42,
    ip: '131.232.99.1',
    labels: {
      'key0' => 'labels2',
      'key1' => 'labels1'
    },
    name: 'my-resource',
    protection: Protection.new(
      delete: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    type: Type50::IPV4,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  action: Action.new(
    command: 'command6',
    error: Error.new(
      code: 'code2',
      message: 'message4',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    finished: 'finished0',
    id: 238,
    progress: 143.26,
    resources: [
      Resource.new(
        id: 198,
        type: 'type0',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Resource.new(
        id: 198,
        type: 'type0',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Resource.new(
        id: 198,
        type: 'type0',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    started: 'started8',
    status: Status::RUNNING,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



