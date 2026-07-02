# V2 Reserved Ips Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBSZXNlcnZlZCUyNTIwSXBzJTI1MjBBY3Rpb25zJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2ReservedIpsActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`Array[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/action.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_reserved_ips_actions_response = V2ReservedIpsActionsResponse.new(
  meta: Meta.new(
    total: 1,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  actions: [
    Action.new(
      completed_at: DateTimeHelper.from_rfc3339('2015-11-21T21:51:09Z'),
      id: 72531856,
      region: Region.new(
        available: true,
        features: [
          'private_networking',
          'backups',
          'ipv6',
          'metadata'
        ],
        name: 'New York 3',
        sizes: [
          's-1vcpu-1gb',
          's-1vcpu-2gb',
          's-1vcpu-3gb',
          's-2vcpu-2gb',
          's-3vcpu-1gb',
          's-2vcpu-4gb',
          's-4vcpu-8gb',
          's-6vcpu-16gb',
          's-8vcpu-32gb',
          's-12vcpu-48gb',
          's-16vcpu-64gb',
          's-20vcpu-96gb',
          's-24vcpu-128gb',
          's-32vcpu-192gb'
        ],
        slug: 'nyc3',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      region_slug: 'nyc3',
      resource_id: 758604197,
      resource_type: 'reserved_ip',
      started_at: DateTimeHelper.from_rfc3339('2015-11-21T21:51:09Z'),
      status: Status1::COMPLETED,
      type: 'reserve_ip',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  links: Links.new(
    pages: Pages.new(
      last: 'last6',
      mnext: 'next2',
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



