# Create Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZVZvbHVtZVJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`CreateVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `automount` | `TrueClass \| FalseClass` | Optional | Auto-mount Volume after attach. `server` must be provided. |
| `format` | `String` | Optional | Format Volume after creation. One of: `xfs`, `ext4` |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `location` | `String` | Optional | Location to create the Volume in (can be omitted if Server is specified) |
| `name` | `String` | Required | Name of the volume |
| `server` | `Integer` | Optional | Server to which to attach the Volume once it's created (Volume will be created in the same Location as the server) |
| `size` | `Integer` | Required | Size of the Volume in GB |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
create_volume_request = CreateVolumeRequest.new(
  name: 'databases-storage',
  size: 42,
  automount: false,
  format: 'xfs',
  labels: { 'labelkey' => 'value' },
  location: 'nbg1',
  server: 110,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



