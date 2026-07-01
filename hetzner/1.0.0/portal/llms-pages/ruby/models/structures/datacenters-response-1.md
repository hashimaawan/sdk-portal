# Datacenters Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkRhdGFjZW50ZXJzJTI1MjBSZXNwb25zZTE


# Class Name

`DatacentersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `datacenter` | [`Datacenter`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/datacenter.md) | Required | - |


# Example

```ruby
datacenters_response1 = DatacentersResponse1.new(
  Datacenter.new(
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
)
```



