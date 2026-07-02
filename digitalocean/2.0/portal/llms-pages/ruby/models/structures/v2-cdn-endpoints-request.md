# V2 Cdn Endpoints Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2CdnEndpointsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate_id` | `UUID \| String` | Optional | The ID of a DigitalOcean managed TLS certificate used for SSL when a custom subdomain is provided. |
| `custom_domain` | `String` | Optional | The fully qualified domain name (FQDN) of the custom subdomain used with the CDN endpoint. |
| `ttl` | [`Ttl`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/ttl.md) | Optional | The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.<br><br>**Default**: `Ttl::ENUM_3600` |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_cdn_endpoints_request = V2CdnEndpointsRequest.new(
  certificate_id: '892071a0-bb95-49bc-8021-3afd67a210bf',
  custom_domain: 'static.example.com',
  ttl: Ttl::ENUM_3600,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



