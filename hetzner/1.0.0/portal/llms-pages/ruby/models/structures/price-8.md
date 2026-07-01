# Price 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaWNlOA


# Class Name

`Price8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `String` | Required | Name of the Location the price is for |
| `price_hourly` | [`PriceHourly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-hourly-7.md) | Required | Hourly costs for a Primary IP type in this Location |
| `price_monthly` | [`PriceMonthly9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-monthly-9.md) | Required | Monthly costs for a Primary IP type in this Location |


# Example

```ruby
price8 = Price8.new(
  'fsn1',
  PriceHourly7.new(
    '1.1900000000000000',
    '1.0000000000'
  ),
  PriceMonthly9.new(
    '1.1900000000000000',
    '1.0000000000'
  )
)
```



