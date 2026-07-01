# Attach Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkF0dGFjaFZvbHVtZVJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`AttachVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `automount` | `TrueClass \| FalseClass` | Optional | Auto-mount the Volume after attaching it |
| `server` | `Integer` | Required | ID of the Server the Volume will be attached to |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
attach_volume_request = AttachVolumeRequest.new(
  server: 43,
  automount: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



