# Price 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlByaWNlOQ


# Class Name

`Price9`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `String` | Required | Name of the Location the price is for |
| `price_hourly` | [`PriceHourly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/price-hourly-8.md) | Required | Hourly costs for a Server type in this Location |
| `price_monthly` | [`PriceMonthly10`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/price-monthly-10.md) | Required | Monthly costs for a Server type in this Location |


# Example

```ruby
price9 = Price9.new(
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
```



