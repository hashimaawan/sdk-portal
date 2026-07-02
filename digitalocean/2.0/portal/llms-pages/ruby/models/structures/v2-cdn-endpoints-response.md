# V2 Cdn Endpoints Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2CdnEndpointsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `endpoints` | [`Array[Endpoint]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/endpoint.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_cdn_endpoints_response = V2CdnEndpointsResponse.new(
  meta: Meta.new(
    total: 1,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  endpoints: [
    Endpoint.new(
      origin: 'static-images.nyc3.digitaloceanspaces.com',
      certificate_id: '892071a0-bb95-49bc-8021-3afd67a210bf',
      created_at: DateTimeHelper.from_rfc3339('2018-07-19T15:04:16Z'),
      custom_domain: 'static.example.com',
      endpoint: 'static-images.nyc3.cdn.digitaloceanspaces.com',
      id: '19f06b6a-3ace-4315-b086-499a0e521b76',
      ttl: Ttl::ENUM_3600,
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



