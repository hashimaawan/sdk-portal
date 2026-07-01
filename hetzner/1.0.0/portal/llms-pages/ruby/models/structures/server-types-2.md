# Server Types 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlclR5cGVzMg


# Class Name

`ServerTypes2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Float` | Required | ID of the Server type the price is for |
| `name` | `String` | Required | Name of the Server type the price is for |
| `prices` | [`Array[Price9]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-9.md) | Required | Server type costs per Location |


# Example

```ruby
server_types2 = ServerTypes2.new(
  4,
  'cx11',
  [
    Price9.new(
      'fsn1',
      PriceHourly8.new(
        '1.1900000000000000',
        '1.0000000000'
      ),
      PriceMonthly10.new(
        '1.1900000000000000',
        '1.0000000000'
      )
    )
  ]
)
```



