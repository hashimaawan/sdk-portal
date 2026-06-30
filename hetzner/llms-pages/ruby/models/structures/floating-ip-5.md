# Floating Ip 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA1


# Class Name

`FloatingIp5`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prices` | [`Array[Price6]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/price-6.md) | Required | Floating IP type costs per Location |
| `type` | [`Type48Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/type-48.md) | Required | The type of the Floating IP |


# Example

```ruby
floating_ip5 = FloatingIp5.new(
  [
    Price6.new(
      'fsn1',
      PriceMonthly7.new(
        '1.1900000000000000',
        '1.0000000000'
      )
    )
  ],
  Type48Enum::IPV4
)
```



