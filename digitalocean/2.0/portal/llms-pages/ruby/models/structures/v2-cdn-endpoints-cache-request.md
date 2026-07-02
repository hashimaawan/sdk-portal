# V2 Cdn Endpoints Cache Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwQ2FjaGUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2CdnEndpointsCacheRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `files` | `Array[String]` | Required | An array of strings containing the path to the content to be purged from the CDN cache. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_cdn_endpoints_cache_request = V2CdnEndpointsCacheRequest.new(
  files: [
    'path/to/image.png',
    'path/to/css/*'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



