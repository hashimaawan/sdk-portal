# Price 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaWNlNg


# Class Name

`Price6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `String` | Required | Name of the Location the price is for |
| `price_monthly` | [`PriceMonthly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-monthly-7.md) | Required | Monthly costs for a Floating IP type in this Location |


# Example

```ruby
price6 = Price6.new(
  'fsn1',
  PriceMonthly7.new(
    '1.1900000000000000',
    '1.0000000000'
  )
)
```



