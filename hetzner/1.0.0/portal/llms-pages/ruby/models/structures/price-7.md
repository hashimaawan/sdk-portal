# Price 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaWNlNw


# Class Name

`Price7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `String` | Required | Name of the Location the price is for |
| `price_hourly` | [`PriceHourly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-hourly-6.md) | Required | Hourly costs for a Load Balancer type in this network zone |
| `price_monthly` | [`PriceMonthly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-monthly-8.md) | Required | Monthly costs for a Load Balancer type in this network zone |


# Example

```ruby
price7 = Price7.new(
  'fsn1',
  PriceHourly6.new(
    '1.1900000000000000',
    '1.0000000000'
  ),
  PriceMonthly8.new(
    '1.1900000000000000',
    '1.0000000000'
  )
)
```



