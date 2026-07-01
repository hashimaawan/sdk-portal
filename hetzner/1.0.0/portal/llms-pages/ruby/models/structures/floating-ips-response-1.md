# Floating Ips Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Object.*


# Class Name

`FloatingIpsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action.md) | Optional | - |
| `floating_ip` | [`FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/floating-ip.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
floating_ips_response1 = FloatingIpsResponse1.new(
  floating_ip: FloatingIp.new(
    blocked: false,
    created: '2016-01-30T23:55:00+00:00',
    description: 'this describes my resource',
    dns_ptr: [
      DnsPtr.new(
        dns_ptr: 'server.example.com',
        ip: '2001:db8::1',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    home_location: HomeLocation.new(
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
    id: 42,
    ip: '131.232.99.1',
    labels: {
      'key0' => 'labels4',
      'key1' => 'labels3',
      'key2' => 'labels2'
    },
    name: 'my-resource',
    protection: Protection.new(
      delete: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    server: 42,
    type: Type16::IPV4,
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



