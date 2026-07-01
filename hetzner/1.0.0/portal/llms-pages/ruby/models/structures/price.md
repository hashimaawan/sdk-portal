# Price

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaWNl

*This model accepts additional fields of type Object.*


# Class Name

`Price`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `String` | Required | Name of the Location the price is for |
| `price_hourly` | [`PriceHourly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-hourly.md) | Required | Hourly costs for a Resource in this Location |
| `price_monthly` | [`PriceMonthly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-monthly.md) | Required | Monthly costs for a Resource in this Location |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
price = Price.new(
  location: 'fsn1',
  price_hourly: PriceHourly.new(
    gross: '1.1900000000000000',
    net: '1.0000000000',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  price_monthly: PriceMonthly.new(
    gross: '1.1900000000000000',
    net: '1.0000000000',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



