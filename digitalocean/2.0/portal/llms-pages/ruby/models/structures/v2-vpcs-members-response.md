# V2 Vpcs Members Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBWcGNzJTI1MjBNZW1iZXJzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2VpcsMembersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `members` | [`Array[Member]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/member.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_vpcs_members_response = V2VpcsMembersResponse.new(
  meta: Meta.new(
    total: 4,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  members: [
    Member.new(
      created_at: '2020-03-13T19:30:48Z',
      name: 'nyc1-load-balancer-01',
      urn: 'do:loadbalancer:fb294d78-d193-4cb2-8737-ea620993591b',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Member.new(
      created_at: '2020-03-13T19:30:18Z',
      name: 'db-postgresql-nyc1-55986',
      urn: 'do:dbaas:13f7a2f6-43df-4c4a-8129-8733267ddeea',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Member.new(
      created_at: '2020-03-13T19:30:16Z',
      name: 'k8s-nyc1-1584127772221',
      urn: 'do:kubernetes:da39d893-96e1-4e4d-971d-1fdda33a46b1',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Member.new(
      created_at: '2020-03-13T19:29:20Z',
      name: 'ubuntu-s-1vcpu-1gb-nyc1-01',
      urn: 'do:droplet:86e29982-03a7-4946-8a07-a0114dff8754',
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



