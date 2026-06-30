# Datacenter

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkRhdGFjZW50ZXI


# Class Name

`Datacenter`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `String` | Required | Description of the Datacenter |
| `id` | `Integer` | Required | ID of the Resource |
| `location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/location.md) | Required | - |
| `name` | `String` | Required | Unique identifier of the Datacenter |
| `server_types` | [`ServerTypes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/server-types.md) | Required | The Server types the Datacenter can handle |


# Example

```ruby
datacenter = Datacenter.new(
  'Falkenstein DC Park 8',
  42,
  Location.new(
    'Falkenstein',
    'DE',
    'Falkenstein DC Park 1',
    1,
    50.47612,
    12.370071,
    'fsn1',
    'eu-central'
  ),
  'fsn1-dc8',
  ServerTypes.new(
    [
      1,
      2,
      3
    ],
    [
      1,
      2,
      3
    ],
    [
      1,
      2,
      3
    ]
  )
)
```



