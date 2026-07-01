# Price 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaWNlNw

*This model accepts additional fields of type Object.*


# Class Name

`Price7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `String` | Required | Name of the Location the price is for |
| `price_hourly` | [`PriceHourly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-hourly-6.md) | Required | Hourly costs for a Load Balancer type in this network zone |
| `price_monthly` | [`PriceMonthly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-monthly-8.md) | Required | Monthly costs for a Load Balancer type in this network zone |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
price7 = Price7.new(
  location: 'fsn1',
  price_hourly: PriceHourly6.new(
    gross: '1.1900000000000000',
    net: '1.0000000000',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  price_monthly: PriceMonthly8.new(
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



