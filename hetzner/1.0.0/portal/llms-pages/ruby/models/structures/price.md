# Price

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaWNl


# Class Name

`Price`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `String` | Required | Name of the Location the price is for |
| `price_hourly` | [`PriceHourly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-hourly.md) | Required | Hourly costs for a Resource in this Location |
| `price_monthly` | [`PriceMonthly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-monthly.md) | Required | Monthly costs for a Resource in this Location |


# Example

```ruby
price = Price.new(
  'fsn1',
  PriceHourly.new(
    '1.1900000000000000',
    '1.0000000000'
  ),
  PriceMonthly.new(
    '1.1900000000000000',
    '1.0000000000'
  )
)
```



