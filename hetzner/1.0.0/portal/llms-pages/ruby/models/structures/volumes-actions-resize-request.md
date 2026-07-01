# Volumes Actions Resize Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMFJlc2l6ZSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`VolumesActionsResizeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `size` | `Float` | Required | New Volume size in GB (must be greater than current size) |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
volumes_actions_resize_request = VolumesActionsResizeRequest.new(
  size: 50,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



