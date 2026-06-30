# Datacenters Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkRhdGFjZW50ZXJzJTI1MjBSZXNwb25zZQ


# Class Name

`DatacentersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `datacenters` | [`Array[Datacenter]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/datacenter.md) | Required | - |
| `recommendation` | `Float` | Required | The Datacenter which is recommended to be used to create new Servers. |


# Example

```ruby
datacenters_response = DatacentersResponse.new(
  [
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
  ],
  1
)
```



