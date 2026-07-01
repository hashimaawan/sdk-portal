# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlZvbHVtZQ

The cost of Volume per GB/month


# Class Name

`Volume`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `price_per_gb_month` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-per-gb-month.md) | Required | - |


# Example

```ruby
volume = Volume.new(
  PricePerGbMonth.new(
    '1.1900000000000000',
    '1.0000000000'
  )
)
```



