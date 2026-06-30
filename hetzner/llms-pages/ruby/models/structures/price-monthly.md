# Price Monthly

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlByaWNlTW9udGhseQ

Monthly costs for a Resource in this Location


# Class Name

`PriceMonthly`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `String` | Required | Price with VAT added |
| `net` | `String` | Required | Price without VAT |


# Example

```ruby
price_monthly = PriceMonthly.new(
  '1.1900000000000000',
  '1.0000000000'
)
```



