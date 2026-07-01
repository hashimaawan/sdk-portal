# Rebuild Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlYnVpbGRTZXJ2ZXJSZXF1ZXN0


# Class Name

`RebuildServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | `String` | Required | ID or name of Image to rebuilt from. |


# Example

```ruby
rebuild_server_request = RebuildServerRequest.new(
  'ubuntu-20.04'
)
```



