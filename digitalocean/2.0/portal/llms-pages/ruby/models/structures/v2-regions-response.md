# V2 Regions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpb25zJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2RegionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `regions` | [`Array[Region]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/region.md) | Required | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_regions_response = V2RegionsResponse.new(
  regions: [
    Region.new(
      available: true,
      features: [
        'private_networking',
        'backups',
        'ipv6',
        'metadata',
        'install_agent',
        'storage',
        'image_transfer'
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
        's-32vcpu-192g'
      ],
      slug: 'nyc3',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  meta: Meta.new(
    total: 13,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  links: Links.new(
    pages: Pages.new(
      last: 'https://api.digitalocean.com/v2/regions?page=13&per_page=1',
      mnext: 'https://api.digitalocean.com/v2/regions?page=2&per_page=1',
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



