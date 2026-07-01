# Price Monthly 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTg

Monthly costs for a Load Balancer type in this network zone

*This model accepts additional fields of type Object.*


# Class Name

`PriceMonthly8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `String` | Required | Price with VAT added |
| `net` | `String` | Required | Price without VAT |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
price_monthly8 = PriceMonthly8.new(
  gross: '1.1900000000000000',
  net: '1.0000000000',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



