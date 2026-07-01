# Floating Ip 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA0

The cost of one Floating IP per month


# Class Name

`FloatingIp4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `price_monthly` | [`PriceMonthly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-monthly-6.md) | Required | - |


# Example

```ruby
floating_ip4 = FloatingIp4.new(
  PriceMonthly6.new(
    '1.1900000000000000',
    '1.0000000000'
  )
)
```



