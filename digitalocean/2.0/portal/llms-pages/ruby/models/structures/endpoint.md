# Endpoint

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkVuZHBvaW50

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Endpoint`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate_id` | `UUID \| String` | Optional | The ID of a DigitalOcean managed TLS certificate used for SSL when a custom subdomain is provided. |
| `created_at` | `DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the CDN endpoint was created. |
| `custom_domain` | `String` | Optional | The fully qualified domain name (FQDN) of the custom subdomain used with the CDN endpoint. |
| `endpoint` | `String` | Optional, Read-only | The fully qualified domain name (FQDN) from which the CDN-backed content is served. |
| `id` | `UUID \| String` | Optional, Read-only | A unique ID that can be used to identify and reference a CDN endpoint. |
| `origin` | `String` | Required | The fully qualified domain name (FQDN) for the origin server which provides the content for the CDN. This is currently restricted to a Space. |
| `ttl` | [`Ttl`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/ttl.md) | Optional | The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.<br><br>**Default**: `Ttl::ENUM_3600` |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
endpoint = Endpoint.new(
  origin: 'static-images.nyc3.digitaloceanspaces.com',
  certificate_id: '892071a0-bb95-49bc-8021-3afd67a210bf',
  created_at: DateTimeHelper.from_rfc3339('2018-03-21T16:02:37Z'),
  custom_domain: 'static.example.com',
  endpoint: 'static-images.nyc3.cdn.digitaloceanspaces.com',
  id: '892071a0-bb95-49bc-8021-3afd67a210bf',
  ttl: Ttl::ENUM_3600,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



