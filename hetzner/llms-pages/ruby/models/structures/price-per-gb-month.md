# Price per Gb Month

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlByaWNlUGVyR2JNb250aA


# Class Name

`PricePerGbMonth`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `String` | Required | Price with VAT added |
| `net` | `String` | Required | Price without VAT |


# Example

```ruby
price_per_gb_month = PricePerGbMonth.new(
  '1.1900000000000000',
  '1.0000000000'
)
```



