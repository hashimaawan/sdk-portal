# Create Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZVZvbHVtZVJlcXVlc3Q


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


# Example

```ruby
create_volume_request = CreateVolumeRequest.new(
  'databases-storage',
  42,
  false,
  'xfs',
  { 'labelkey' => 'value' },
  'nbg1',
  110
)
```



