# Traffic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlRyYWZmaWM

The cost of additional traffic per TB


# Class Name

`Traffic`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `price_per_tb` | [`PricePerTb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-per-tb.md) | Required | - |


# Example

```ruby
traffic = Traffic.new(
  PricePerTb.new(
    '1.1900000000000000',
    '1.0000000000'
  )
)
```



