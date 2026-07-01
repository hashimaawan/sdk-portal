# Rebuild Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlYnVpbGRTZXJ2ZXJSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`RebuildServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | `String` | Required | ID or name of Image to rebuilt from. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
rebuild_server_request = RebuildServerRequest.new(
  image: 'ubuntu-20.04',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



