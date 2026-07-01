# Price Monthly 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTc

Monthly costs for a Floating IP type in this Location

*This model accepts additional fields of type Object.*


# Class Name

`PriceMonthly7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `String` | Required | Price with VAT added |
| `net` | `String` | Required | Price without VAT |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
price_monthly7 = PriceMonthly7.new(
  gross: '1.1900000000000000',
  net: '1.0000000000',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



