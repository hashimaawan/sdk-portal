# V2 Reserved Ips Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBSZXNlcnZlZCUyNTIwSXBzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2ReservedIpsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `links` | [`Links3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/links-3.md) | Optional | - |
| `reserved_ip` | [`ReservedIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/reserved-ip.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_reserved_ips_response1 = V2ReservedIpsResponse1.new(
  links: Links3.new(
    actions: [
      Action1.new(
        href: 'href0',
        id: 154,
        rel: 'rel4',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    droplets: [
      Action1.new(
        href: 'href2',
        id: 232,
        rel: 'rel6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Action1.new(
        href: 'href2',
        id: 232,
        rel: 'rel6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  reserved_ip: ReservedIp.new(
    droplet: { 'key1' => 'val1', 'key2' => 'val2' },
    ip: 'ip6',
    locked: false,
    project_id: '00002548-0000-0000-0000-000000000000',
    region: Region.new(
      available: false,
      features: [
        'features7',
        'features8',
        'features9'
      ],
      name: 'name6',
      sizes: [
        'sizes6'
      ],
      slug: 'slug0',
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



